# 2.5 Arduino Time Functions

## 2.5.1 void delay(ms);
* **brief**: delay several milliseconds.
* **param**:
    - **ms**: milliseconds to delay.
* **return**: void.

## 2.5.2 void delayMicroseconds(us);
* **brief**: delay several microseconds.
* **param**:
    - **us**: microseconds to delay.
* **return**: void.

## 2.5.3 unsigned long millis();
* **brief**: return the time length in milliseconds since the most recent rebooting. Clearly, the longest time that can be recorded is 2^32-1 milliseconds. After that, the time length will starts from 0 again.
* **param**:
    - void
* **return**: unsigned long.

## 2.5.4 unsigned long micros();
* **brief**: return the time length in microseconds since the most recent rebooting. Clearly, the longest time that can be recorded is 2^32-1 microseconds. After that, the time length will starts from 0 again.
* **param**:
    - void
* **return**: unsigned long.
