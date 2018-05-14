# 2.2 FIRST STM32 Project - "Hello World"

As any other programming languages, our first STM32 Project is also "Hello World", without hardware wiring. Using GNU MCU Eclipse to develop STM32 follows the same way to develop any other projects under Eclipse.

## Sketch

The code can be found at [Examples_STM32F767ZI - geek-workshop - studynotes - _001_HelloWorld - _001_HelloWorld.ino](https://github.com/LongerVisionRobot/Examples_Arduino/blob/master/geek-workshop/studynotes/_001_HelloWorld/_001_HelloWorld.ino).
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

![Eclipse New Projects](./Eclipse_01_New_Projects.jpg)


![Eclipse Create STM32FXX Projects](./Eclipse_02_New_Projects_STM32F7XX.jpg)


![Eclipse Target Processor Settings](Eclipse_03_Target_Processor_Settings.jpg)


![Eclipse Folders Settings](Eclipse_04_Folders_Settings.jpg)


![Eclipse Select Configurations](Eclipse_05_Select_Configurations.jpg)


![Eclipse GNU ARM Cross Toolchain](Eclipse_06_GNU_ARM_Cross_Toolchain.jpg)


![Eclipse Built Failure](Eclipse_07_Built_Failure.jpg)


![Eclipse Successfully Built](Eclipse_08_Successfully_Built.jpg)


![--specs=nosys.specs](Project_Properties_C++Build_Settings_ToolSettings_Linker_Miscellaneous.jpg)


