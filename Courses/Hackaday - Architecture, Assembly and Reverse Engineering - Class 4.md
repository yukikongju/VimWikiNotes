## Hackaday - Architecture, Assembly and Reverse Engineering - Class 4

### Overview

1. Example - Fibonacci
2. View Assembly Compiled Code
3. Debuging with GDB

### Part 1 - Fibonacci in Assembly

###### arduino.ino

```
#define LED 1

extern "C" uint8_t fibo(uint8_t number);

void setup() {
  Serial.begin(115200);

// print the first 10 fibonacci numbers
  for(int i=0; i<10 ; i++){
      Serial.println(fibo(i));
  }

}

void loop() {
}
```

###### assembly.S

```
; arg1: r24, result: r24
; if n==0 return 0
; if n==1 return 1
; fibo(n-1)
; fibo(n-2)
; return fibo(n-1)+fibo(n-2)
.global fibo
fibo:
  cpi r24, 0
  breq 1f
  cpi r24, 1
  breq 1f
  dec r24
  push r24      ; (n-1)
  call fibo
  mov r18, r24  ; copy fibo(n-1) into r18
  pop r24       ; (n-1)
  push r18      ; save fibo(n-1) in the stack
  dec r24       ; (n-2)
  call fibo     ; r24 <- fibo(n-2)
  pop r23       ; fibo(n-1) -> WHY IS IT IN r23????: pop the stack and store it in r23
  add r24, r23  ; fibo(n-2) + fibo(n-1)
1:
  ret
```

### Part 2 - Reading Assembly Compiled Code

We can view our compiled code with `` avr-objdump `` or with wokwi `` <F1> Assembly Compiled Code ``

Remarks:
- If we iterate for less than 5 iterations, the wokwi compiler unroll the instructions. It only creates a loop for 6+ iterations.

### Part 3 - Debuging with GDB

To run debuger in wokwi, run `` <F1> gdb (release build)``

To see all gdb command: [Arduino/AVR GDB Cheat Sheet](https://blog.wokwi.com/gdb-avr-arduino-cheatsheet/)
Useful Commands:
- list <funct>:
- backtrace:
- layout asm: popup window to scroll code
- layout split: view compiled code and C code
- focus next: change window
- next/step/nexti
- print $r0: print register
- info breaks

### Ressources

- [Arduino/AVR GDB Cheat Sheet](https://blog.wokwi.com/gdb-avr-arduino-cheatsheet/)

