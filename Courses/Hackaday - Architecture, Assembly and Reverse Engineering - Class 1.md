## Hackaday - Architecture, Assembly and Reverse Engineering - Class 1

### Overview

This class introduces us to Aduino in two ways: using Arduino functions and using bit registers. We saw 3 sections:
1. Registers
2. Interrupts
3. Timers

All the code will be written using the Wokwi Arduino Simulator

### Part 1 - Registers

AVR contains 2 memory space: Data Memory Register and Program Memory register. The former store the data whilst the latter store the pointers.

We can work with Arduino functions: `` Serial.begin()`` and ``digitalWrite()``. However, we would like to use registers to write our code. Instead of referencing PINS, we want to reference ports. According to the documentation (section 14), each pins can be mapped to its port.

We can look at Arduino datasheet to check pins and port equivalence. For example, pin D13 correspond to PB5. We can then look at AVR documentation to see how to map PB5 to registers.

To see address of variable: `` Serial.println((int) &value, HEX/BIN); ``

We can also define DDRD so that we can control all the LED at the same time:
`` DDRD = 0b11111111;``

Remarks:
- ``   Serial.println(bit(7), BIN); `` is equivalent to `` Serial.println(136, BIN);``
- `` DDRB = bit(5);`` is equivalent to `` pinMode(LED_BUILTIN, OUTPUT);``
- `` bitSet(PORTB, 5);`` is equivalent to `` digitalWrite(LED_BUILTIN, HIGH);``
- `` bitClear(PORTB, 5);`` is equivalent to `` digitalWrite(LED_BUILTIN, LOW);``


##### Example: LED Blink

###### Arduino Environment Code

```arduino
void setup() {
  // initialize digital pin LED_BUILTIN as an output.
    pinMode(LED_BUILTIN, OUTPUT);
    Serial.begin(115200);
}

// the loop function runs over and over again forever
void loop() {
  digitalWrite(LED_BUILTIN, HIGH);   // turn the LED on (HIGH is the voltage level)
    delay(1000);                       // wait for a second
  digitalWrite(LED_BUILTIN, LOW);    // turn the LED off by making the voltage LOW
  delay(1000);                       // wait for a second
}
```

###### Registers Code

```
void setup() {
    DDRB = bit(5);
}

void loop() {
    bitSet(PORTB, 5);
    delay(1000);
    bitClear(PORTB, 5);
    delay(1000);
}
```

### Part 2 - Interrupts

Interrupts are what controls the instructions we give to the arduino. We can use the functions ``sei()`` and ``cli()`` to enable and disable interrupts. It should be noted that interrupts are initially enabled.

##### Example: Liquid Crystal Switch Interrupts

### Part 3 - Timers

We can control clock speed using `` TCCR1A()``, `` TCCCR1B()``, `` TCCR1C``

### Ressources

- [AVR ATmega48A Documentation](https://www.tme.com/Document/96b6778db42cd7ee25e95be3e9a8b195/atmegaxx8apa.pdf)
