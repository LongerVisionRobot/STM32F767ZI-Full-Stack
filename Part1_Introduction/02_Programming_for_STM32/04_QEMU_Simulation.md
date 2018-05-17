# 2.4 QEMU Simulation (Optional)

In the [previous section](../02_Programming_for_STM32/02_hello_world.md), we have **NOT** run/test/debug the program yet. How to do that? Normally, there are 2 ways to test your code before flashing your code down to a chip. 
* **Way 1**: Test in a simulator, which simulates the **STM32** chip
* **Way 2**: Test on a real **STM32** development board

In this section, we are going to talk about how to run/test/debug the program in the popular simulator [**QEMU**](https://www.qemu.org/).


## 2.4.1 QEMU Installation

### Ways to Install QEMU

#### Option 1: Official Installation

You can directly download QEMU's **NEWEST** release from its official website [https://www.qemu.org](https://www.qemu.org).

#### Option 2: Ubuntu Repository (Our Way)

One command will do:
```
$ sudo apt install qemu
```

#### Option 3: GNU MCU Eclipse QEMU

Since in our course, we are using [GNU MCU Eclipse Plugin](https://gnu-mcu-eclipse.github.io/), we can also use [its own QEMU simulator](https://gnu-mcu-eclipse.github.io/qemu/install/), from whree we should be able to find its [releases on Github](https://github.com/gnu-mcu-eclipse/qemu/releases). However, its **NEWEST** release is **v2.8.0-20170301**, which is quite **OLD**.


#### Option 4: Build from Source (Recommended)

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


### Test QEMU


