# Hackaday - Architecture, Assembly and Reverse Engineering - Class 2

### Overview

This lecture has 3 parts:
1. Timers - How to use timers to change clock speed
2. Assembly Instructions - How to write Assembly code in Arduino

### Part 1 -  Timers - How to use timers to change clock speed

### Part 2 - Assembly Instructions - How to write Assembly code in Arduino

###### What are the assembly registers

There are 31 8-bits registers (r0...r31). Some of these registers have special names:

- X: (r26,r27)
- Y: (r28,r29)
- Z: (r30,r31)
- PC: Program Counter
- SREG: Status Register

###### Assembly Instructions in Arduino

Arduino Instructions has the following syntax: `` asm("<INSTRUCTION>"); ``

We have seen a few instructions:
- NOP: ``ams("NOP");``
- CLI/SEI: ``ams("CLI");``, ``ams("SEI"); ``
- BREAK: ``ams("BREAK");``
- LDI/LDS: ``ams("LDI r16, 55");``
- STS/STD: ``ams("STS 286, r16");``
- INC: ``ams("NOP");``

All instructions can be found at [ATmega48A Instructions](http://ww1.microchip.com/downloads/en/DeviceDoc/AVR-Instruction-Set-Manual-DS40002198A.pdf)

###### Assembly Instructions - Input and Output

We can also read and write using assembly languages. The syntax is as follow:

`` asm("<INST>" : "<WRITE>" : "<READ>"); ``

We can specify value and address as follows:

```arduino
asm("STS %[addr], %[val]"
    : /* write */
    : /* read */ [val]"r"[value], [addr]"M"(&PORTD)
);
```

"r": read registers
"M": integer constants

### Ressources

- [ATmega48A Instructions](http://ww1.microchip.com/downloads/en/DeviceDoc/AVR-Instruction-Set-Manual-DS40002198A.pdf)
- [AVR User Manual](https://www.nongnu.org/avr-libc/user-manual/inline_asm.html)
