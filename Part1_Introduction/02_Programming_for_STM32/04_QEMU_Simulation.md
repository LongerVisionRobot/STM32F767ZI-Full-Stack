# 2.4 QEMU Simulation (Optional)

In the [previous section](../02_Programming_for_STM32/02_hello_world.md), we have **NOT** run/test/debug the program yet. How to do that? Normally, there are 2 ways to test your code before flashing your code down to a chip. 
* **Way 1**: Test in a simulator, which simulates the **STM32** chip
* **Way 2**: Test on a real **STM32** development board

In this section, we are going to talk about how to run/test/debug the program in the popular simulator [**QEMU**](https://www.qemu.org/).


## 2.4.1 QEMU Installation

### Ways to Install QEMU

#### Option 1: Official Installation

You can directly download QEMU's **NEWEST** release from its official website [https://www.qemu.org](https://www.qemu.org).

#### Option 2: Ubuntu Repository

One command will do:
```
$ sudo apt install qemu
```


#### Option 3: Build from Source (Recommended)

This option is adopted in our case. Just strictly follow [https://www.qemu.org/download/#source](https://www.qemu.org/download/#source):
```
git clone git://git.qemu.org/qemu.git
cd qemu
git submodule init
git submodule update --recursive
mkdir build
cd build
../configure
make -j4
```


#### Option 4: GNU MCU Eclipse QEMU (Our Way)

Since in our course, we are using [GNU MCU Eclipse Plugin](https://gnu-mcu-eclipse.github.io/), we also use [its own QEMU simulator](https://gnu-mcu-eclipse.github.io/qemu/install/), from where we should be able to find its [releases on Github](https://github.com/gnu-mcu-eclipse/qemu/releases). However, its **NEWEST** release is **v2.8.0-20170301**, which is quite **OLD**. According to [GNU MCU Eclipse QEMU](https://gnu-mcu-eclipse.github.io/qemu/), its current supported boards and MCUs:

**Supported Boards**:
* **Maple** - LeafLab Arduino-style STM32 microcontroller board
* **NUCLEO-F103RB** - ST Nucleo Development Board for STM32 F1 series
* **NetduinoGo** - Netduino GoBus Development Board with STM32F4
* **NetduinoPlus2** - Netduino Development Board with STM32F4
* **STM32-E407** - Olimex Development Board for STM32F407ZGT6
* **STM32-H103** - Olimex Header Board for STM32F103RBT6
* **STM32-P103** - Olimex Prototype Board for STM32F103RBT6
* **STM32-P107** - Olimex Prototype Board for STM32F107VCT6
* **STM32F4-Discovery** - ST Discovery kit for STM32F407/417 lines
* **STM32F429I-Discovery** - ST Discovery kit for STM32F429/439 lines

**Supported MCUs**:
* **STM32F103RB**
* **STM32F107VC**
* **STM32F405RG**
* **STM32F407VG**
* **STM32F407ZG**
* **STM32F429ZI**
* **STM32L152RE**



### Test QEMU

As mentioned above, since current [GNU MCU Eclipse QEMU](https://gnu-mcu-eclipse.github.io/qemu/) does **NOT** support **STM32F767ZI** yet, we have to carry our QEMU test with another board. Here, we pick up board **STM32F429I-Discovery** with MCU **STM32F429ZI** to carry out QEMU test.


