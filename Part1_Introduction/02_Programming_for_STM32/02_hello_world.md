# 2.2 FIRST STM32 Project - "Hello World"

As any other programming languages, our first STM32 Project is also "Hello World", without hardware wiring. The code follows standard STM32 coding convention, namely, composed of a **setup()** function and a **loop()** function.

## Sketch

The code can be found at [Examples_Arduino - geek-workshop - studynotes - _001_HelloWorld - _001_HelloWorld.ino](https://github.com/LongerVisionRobot/Examples_Arduino/blob/master/geek-workshop/studynotes/_001_HelloWorld/_001_HelloWorld.ino).
```
void setup() {
  Serial.begin(9600); // Open serial port, and set bit rate to 9600.  
}

void loop() {
  Serial.println("Hello World"); // output "Hello World" to serial port.
  delay(1000); // wait for a second
}
```

## Verify & Compile

In Arduino IDe, to compile the above codes, click **Sketch->Verify/Compile**; to upload the code onto Arduino board afterwards, click **Sketch->Upload**.
