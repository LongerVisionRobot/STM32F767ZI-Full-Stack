# 2.6 Arduino Interrupt Functions

## 2.6.1 void interrupts();
* **brief**: re-enable interrupts after having been disabled by function **noInterrupts()**.
* **param**: void
* **return**: void.

## 2.6.2 void noInterrupts();
* **brief**: disable interrupts.
* **param**: void
* **return**: void.

## 2.6.3 void attachInterrupt(digitalPinToInterrupt(pin), ISR, mode);
* **brief**: attach interrupt to some particular digital pin. Whenever there is an interrupt, function ISR will be called.
* **param**:
    - **digitalPinToInterrupt(pin)**: an interrupt is normally triggered from a particular **pin**.
    - **ISR**: Interrupt Service Routine, a function has **NO** parameters and has **NO** return value.
    - **mode**: **LOW**, **HIGH**, **CHANGE**, **RISING** or **FALLING**.
        1. **LOW**： trigger the interrupt whenever the pin is at low-level.
        2. **HIGH**: trigger the interrupt whenever the pin is at high-level.
        3. **CHANGE**: trigger the interrupt whenever the pin changes from **HIGH** to **LOW**, or from **LOW** to **HIGH**.
        4. **RISING**: trigger the interrupt whenever the pin changes from **LOW** to **HIGH**.
        5. **FALLING**: trigger the interrupt whenever the pin changes from **HIGH** to **LOW**.
* **return**: void.

## 2.6.4 void detachInterrupt(digitalPinToInterrupt(pin));
* **brief**: detach interrupt from some particular digital pin.
* **param**:
    - **digitalPinToInterrupt(pin)**: an interrupt is normally triggered from a particular **pin**.
* **return**: void.