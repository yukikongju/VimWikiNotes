# Class 1: Compilation, x86_64 instructions, intro to Ghidra

### Overview

This lecture has 3 parts:
1. Compilation: Understand the pipeline for compilation
2. Computer Architecture and x86_64 instructions: understand how a program is executed and the instructions calls in assembly
3. Ghidra: NSA program that decompiles and disassemble binary files

Definitions:
- Disassembler: translate machine code to assembly code
- Decompiler: translate assembly code to pseudo c code

### What is Reverse Engineering

Reverse Engineering is the process of taking the output file of a program and try to understand what performs. To do so, we can use several tools: objdump, dumpelf, readelf, elfutils.

Because this course is based on a linux system, we will work with x86_64 assembly language and elf files. However, it should be noted that different OS produces different output files:
- Windows: PE
- Linux: ELF
- Mac-OS:

### Part 1 - Understanding Compilation

Computer understand binary code (0 and 1). However, we don't write code with 0 and 1. Consequently, we need to translate our code to machine code using compilation.

There are 4 steps in compilation:
1. Precompile: writing in "higher" language (ex:C)
2. Compilation: translate C code to assembly
3. Assembly: translate Assembly code to machine code
4. Linking: Add adresses and metadata so that OS knows where to execute code

### Part 2 - Computer Architecture 101 and x86_64 instructions

There are two goals in this section :
1. Understand how a program is executed
2. Assembly Instructions
3. Understanding how the stack works


###### Understand how a program is executed

When a program executes, it:
1. loaded into memory
2. call instructions in ALU
3. Store output in register or memory

###### Assembly instructions

In x86_64, there are 16 64 bytes registers. We also have several pointers:
- RIP: Instruction pointer, which points to next instruction
- RSP: Stack pointer, which points to the top of the stack
- RBP: Bottom Stack pointer, which points to the bottom of the stack

There are 6 instructions:
1. mov rax, rbx: copy rbx to rax
2. add/sub rax, rbx: rax += rbx
3. Operators: and, or, xor
4. push/pop: add remove element to top of stack and increment/decremtn RSP by 8
5. call: call function
6. compare: cmp -> compare two registers and set flags (jnz, jz)

It should be noted that there are two ways to declare instruction:
- move value STORED: mov rax, rbx
- move value POINTED: mov rax, [rbx]

### Part 3 - Ghidra

Ghidra is an NSA program that became open source in 2019 that can decompile and disassemble binary files.
