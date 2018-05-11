# 2.2 Arduino Digital IO

## 2.2.1 void pinMode(pin, mode);
* **brief**: set **mode** for a particular **pin**.
* **param**:
    - **pin**: digital IO pin index, must be a value between 0 and 19, but 2 ~ 13 is preferred. Normally, pin number should be 0 ~ 13. Analog pins A0 ~ A5 can also be adopted, which is according to number 14 ~ 19.
    - **mode**: **INPUT** or **OUTPUT**, where **INPUT** is for reading, **OUTPUT** is for writing.
* **return**: void.

## 2.2.2 void digitalWrite(pin, value);
* **brief**: write **value** to a particular **pin**.
* **param**:
    - **pin**: digital IO pin index, must be a value between 0 and 19, but 2 ~ 13 is preferred. Normally, pin number should be 0 ~ 13. Analog pins A0 ~ A5 can also be adopted, which is according to number 14 ~ 19.
    - **value**: **HIGH** or **LOW**, where **HIGH** is for high level voltage, **LOW** is for low level voltage.
* **return**: void.

## 2.2.3 int digitalRead(pin);
* **brief**: read the digital **value** from a particular **pin**.
* **param**:
    - **pin**: digital IO pin index, must be a value between 0 and 19, but 2 ~ 13 is preferred. Normally, pin number should be 0 ~ 13. Analog pins A0 ~ A5 can also be adopted, which is according to number 14 ~ 19.
* **return**: either **HIGH(1)** or **LOW(0)**, where **HIGH** is for high level voltage, **LOW** is for low level voltage.