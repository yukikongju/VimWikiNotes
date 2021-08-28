# Hackaday - Architecture, Assembly and Reverse Engineering - Class 5

### Overview

1. Data Space vs I/O Space
2. Port and Pins helper methods with <avr/io.h> and _SFR_IO_ADDR
3. Working with MAX7219

### Part 1 - Data Space vs I/O Space

### Part 2 - Port and Pins helper methods with <avr/io.h> and _SFR_IO_ADDR

Rappel 1: `` mov r18, 0x55 `` is equivalent to `` sts 18, 0x55 ``
Rappel 2: In ``.ino`` file, ``PORTD = 0xff`` make all pins behave similrly

Instead of referencing port by their addresses by looking it up in the documentation, we can use ``<avr/io.h>`` and ``_SFR_IO_ADDR()``

Without: ``<avr/io.h>``
```
sts 0x2b, r24
```

With: ``<avr/io.h>``
```
sts PORTD, r24 /* PORTD = 0x2b */
sts _SFR_IO_ADDR(PORTD), r24
```

### Part 3 - Working with MAX7219

In the setup, we have ``SPI.begin()``. We only have to edit loop().

In the loop, we define a `transaction`, which make a block of LED blinks or not. For each transaction, we send 2 bytes: the first one select the row; the second one select the pins in the row.

To start a transaction, we must set the pin to low; to end a transaction, we must set it to high.

```
void setup(){
    SPI.begin();
}

void loop() {
    // start transaction
    digitalWrite(PIN, LOW); // start transaction
    SPI.transfer(2):	    // select second row
    SPI.transfer(0xff);	    // light entire row
    digitalWrite(PIN, HIGH); // end transaction
}
```

### Part 4 - Simon Says in Assembly


