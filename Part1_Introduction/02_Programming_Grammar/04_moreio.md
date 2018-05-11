# 2.4 More about Arduino IO

## 2.4.1 void tone(pin, frequency, duration);
* **brief**: generates a square wave of the particular frequency on a pin (at a 50%　duty cycle).
* **param**:
    - **pin**: analog IO pin index, must be a value between 0 and 5, corresponding to analog pin A0 ~ A5.
    - **frequency**: **HIGH** or **LOW**. **HIGH** refers to a high level pulse, entering and leaving at a high level voltage; **LOW** refers to a low level pulse, entering and leaving at a low level voltage.
    - **duration (optional)**: **ms** to wait for the pulse to be completed.
* **return**: void.

## 2.4.2 void noTone(pin);
* **brief**: stop generating a generated square wave triggered by **tone()**. Has no effect at all if no tone has been generated..
* **param**:
    - **pin**: analog IO pin index, must be a value between 0 and 5, corresponding to analog pin A0 ~ A5.
* **return**: void.

## 2.4.3 void shiftOut(dataPin, clockPin, bitOrder, value);
* **brief**: shift out a byte bit by bit.
* **param**:
    - **dataPin**: digital IO pin index, must be a value between 0 and 19, but 2 ~ 13 is preferred. Normally, pin number should be 0 ~ 13. Analog pins A0 ~ A5 can also be adopted, which is according to number 14 ~ 19. **dataPin** is the pin each bit is output to.
    - **clockPin**: after the **dataPin** has been set to the correct value, this **clockPin** is to be toggle once.
    - **bitOrder**: either **MSBFIRST** or **LSBFIRST**, corresponding to **Most Significant Bit First** or, **Least Significant Bit First**.
    - **value**: the data to shift out a byte.
* **return**: void.

## 2.4.4 byte shiftIn(dataPin, clockPin, bitOrder);
* **brief**: read pulse length in **ms**.
* **param**:
    - **dataPin**: digital IO pin index, must be a value between 0 and 19, but 2 ~ 13 is preferred. Normally, pin number should be 0 ~ 13. Analog pins A0 ~ A5 can also be adopted, which is according to number 14 ~ 19. **dataPin** is the pin each bit is input from.
    - **clockPin**: before starting reading **dataPin**, this **clockPin** is to be toggle once.
    - **bitOrder**: either **MSBFIRST** or **LSBFIRST**, corresponding to **Most Significant Bit First** or, **Least Significant Bit First**.
* **return**: byte.

## 2.4.5 unsigned long PulseIn(pin, value, timeout);
* **brief**: read pulse length in **ms**.
* **param**:
    - **pin**: analog IO pin index, must be a value between 0 and 5, corresponding to analog pin A0 ~ A5.
    - **value**: **HIGH** or **LOW**. **HIGH** refers to a high level pulse, entering and leaving at a high level voltage; **LOW** refers to a low level pulse, entering and leaving at a low level voltage.
    - **timeout (optional)**: **ms** to wait for the pulse to be completed.
* **return**: unsigned long.