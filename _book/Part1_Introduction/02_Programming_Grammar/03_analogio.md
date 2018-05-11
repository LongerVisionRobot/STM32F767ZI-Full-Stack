# 2.3 Arduino Analog IO

## 2.3.1 void analogReference(type);
* **brief**: set analog reference voltage to a particular value according to different **type**. 
    - **DEFAULT**: 5 Volt; 
    - **INTERNAL**: 2.56 Volt
    - **EXTERNAL**: get the voltage value via **AREF pin**. There must be a 5K ohm pull-up resistor．
* **param**:
    - **type**: **DEFAULT**, **INTERNAL** or **EXTERNAL**.
* **return**: void.

## 2.3.2 int analogRead(pin);
* **brief**: read analog voltage from a particular **pin**, at a period about **100US**.
* **param**:
    - **pin**: analog IO pin index, must be a value between 0 and 5, corresponding to analog pin A0 ~ A5.
* **return**: int, between 0 and 1023.

## 2.3.3 void analogWrite(pin, value);
* **brief**: write voltage **value** to **pin**, by PWM.
    - Arduino PWM is typically of frequency **490HZ**.
    - On an Arduino UNO, digital pins 3, 5, 6, 9, 10, 11 with a **~** sign support PWM analog output.
    - PWM output is of 8 bits, namely, a value between 0 and 255.
* **param**:
    - **pin**: analog IO pin index, must be a value between 0 and 5, corresponding to analog pin A0 ~ A5.
    - **value**: **HIGH** or **LOW**, where **HIGH** is for high level voltage, **LOW** is for low level voltage.
* **return**: void.