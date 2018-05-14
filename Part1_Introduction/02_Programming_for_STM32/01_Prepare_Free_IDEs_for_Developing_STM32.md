# 2.1 Prepare Free IDEs for Developing STM32

## 2.1.1 GNU MCU Eclipse

It's supposed that students have already installed [Eclipse](https://www.eclipse.org). For the time being, the most recent Eclipse release is [Eclipse Oxygen 3A](https://www.eclipse.org/downloads/packages/release/Oxygen/3A), and what we are using is [Eclipse IDE for C/C++ Developers - Linux 64-bit](http://www.eclipse.org/downloads/download.php?file=/technology/epp/downloads/release/oxygen/3a/eclipse-cpp-oxygen-3a-linux-gtk-x86_64.tar.gz).

According to [GNU MCU Eclipse](https://gnu-mcu-eclipse.github.io/):
> GNU MCU Eclipse is an open source project that includes a family of Eclipse plug-ins and tools for multi-platform embedded [ARM](https://www.arm.com/) and [RISC-V](https://riscv.org/) development, based on GNU toolchains. This project is hosted on [GitHub](https://github.com/gnu-mcu-eclipse). The former project was hosted on [GitHub](https://github.com/gnuarmeclipse) and [SourceForge](http://sourceforge.net/projects/gnuarmeclipse/).

The right-hand sidebar on [GNU MCU Eclipse](https://gnu-mcu-eclipse.github.io/) clearly summarizes what's needed to be installed, as in the following image:

![GNU MCU Eclipse: What's To Be Installed](./GNU_MCU_Eclipse_2B_Installed.jpg)

Four things are to be installed:
* [Eclipse Plug-in](https://gnu-mcu-eclipse.github.io/plugins/download/)
* [ARM toolchain](https://gnu-mcu-eclipse.github.io/toolchain/arm/install/)
* [J-Link](https://gnu-mcu-eclipse.github.io/debug/jlink/install/)
* [ST-Link](https://github.com/texane/stlink)


[Github Eclipse Plugins](https://github.com/gnu-mcu-eclipse/eclipse-plugins)


## 2.1.2 SW4STM32 (System Workbench for STM32)

To install the free IDE [System Workbench for STM32](http://www.st.com/en/development-tools/sw4stm32.html), [ST's official website](http://www.st.com/en/development-tools/sw4stm32.html) is redirected to [OpenSTM32](http://www.openstm32.org/). Users must first register on [OpenSTM32](http://www.openstm32.org/), and then strictly follow [Installing System Workbench for STM32](http://www.openstm32.org/Installing%2BSystem%2BWorkbench%2Bfor%2BSTM32).

Since we are going to use [2.1.1 GNU MCU Eclipse](https://gnu-mcu-eclipse.github.io/) through out our course, we are **NOT** going to elaborate the details on how to carry out the development for STM32 using [System Workbench for STM32](http://www.st.com/en/development-tools/sw4stm32.html).
