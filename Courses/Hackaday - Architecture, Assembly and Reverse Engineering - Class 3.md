# Hackaday - Architecture, Assembly and Reverse Engineering - Class 3

### Overview

There are n parts to this class:
1. Assembly Instructions - More Instructions
2. Assembly Instructions - Conditional Branches
3. Importing Assembly file in Arduino

### Part 1 - Assembly Instructions

- INC / DEC
- LSL / LSR (Shift right / left)
- COM (bitwise not) - as opposed to NEG (negate, 2’s comp)
- SWAP (nibbles)
- SBR / CBR (set / clear bits)
- ADD / SUB
- AND / OR / EOR (xor) - bitwise operations
- CP - Compare two registers
- BRSH (and other branches)
- CPI - Compare with Immediate
- CALL / RET
- SBIW (bonus) - Subtract Immediate from Word

Template:

```arduino
asm(R"(
    mov %[result], %[val]
    inc %[result]
    BREAK

  )"
      : /* write */ [result]"=r"(value)
      : /* read */ [val]"r"(value)
);
```

### Part 2 - Assembly Instructions: Conditional Branches

Template:

```arduino
asm(R"(
    CP %[left], %[right]
    BRGE 1f
    mov %[result], %[right]
    jmp  2f
1:
    mov %[result], %[left]
2:
)"
    : [result]"=r"(result)
    : [left]"r"(left), [right]"r"(right)
)

```
### Part 3 - GCC Applications Binary Interface

Instead of writing our assembly code in our arduino file, we may want to create its own assembly file that will be read in our arduino file.

When writting C function `` fct(long a, long b); ``, we should know that the variables ``a`` and ``b`` are stored in different registers depending on variables types.

See: [Calling Conventions](https://gcc.gnu.org/wiki/avr-gcc)

###### Importing assembly files

```
extern "C" uint8_t max8(uint8_t left, uint8_t right);
extern "C" uint8_t swap(uint8_t);
```

###### Writing assembly file

```
.global swap
; arg1:r24, result: r24
swap:
    ldi r24, 13
    ldi r22, 1
    call digitalWrite
    swap r24
    ret

.global max8
; arg1: r24, arg2: r22, result: r24
max8:
    cp r24, r22
    brsh 1f
    mov r24, r22
1:
    ret
```
