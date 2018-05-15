# 2.2 Prepare Free IDEs for Developing STM32

## 2.2.1 GNU MCU Eclipse


### Step 1: Install Eclipse

It's supposed that students have already installed [Eclipse](https://www.eclipse.org). For the time being, the most recent Eclipse release is [Eclipse Oxygen 3A](https://www.eclipse.org/downloads/packages/release/Oxygen/3A), and what we are using is [Eclipse IDE for C/C++ Developers - Linux 64-bit](http://www.eclipse.org/downloads/download.php?file=/technology/epp/downloads/release/oxygen/3a/eclipse-cpp-oxygen-3a-linux-gtk-x86_64.tar.gz).


### Step 2: Install GNU MCU Plug-ins for Eclipse

According to [GNU MCU Eclipse](https://gnu-mcu-eclipse.github.io/):
> GNU MCU Eclipse is an open source project that includes a family of Eclipse plug-ins and tools for multi-platform embedded [ARM](https://www.arm.com/) and [RISC-V](https://riscv.org/) development, based on GNU toolchains. This project is hosted on [GitHub](https://github.com/gnu-mcu-eclipse). The former project was hosted on [GitHub](https://github.com/gnuarmeclipse) and [SourceForge](http://sourceforge.net/projects/gnuarmeclipse/).

The right-hand sidebar on [GNU MCU Eclipse](https://gnu-mcu-eclipse.github.io/) clearly summarizes what's needed to be installed, as in the following image:

![GNU MCU Eclipse: What's To Be Installed](./GNU_MCU_Eclipse_2B_Installed.jpg)

According to our summation, five things are to be installed:
* [Eclipse Plug-in](https://gnu-mcu-eclipse.github.io/plugins/download/)
* [ARM toolchain](https://gnu-mcu-eclipse.github.io/toolchain/arm/install/)
* [J-Link](https://gnu-mcu-eclipse.github.io/debug/jlink/install/)
* [ST-Link](https://github.com/texane/stlink)


#### A. Install Eclipse Plug-in

Currently, if you install the plugin from within Eclipse by providing the plugin's update site URL [http://gnu-mcu-eclipse.netlify.com/v4-neon-updates](http://gnu-mcu-eclipse.netlify.com/v4-neon-updates), you will possibly meet the following error message:

![GNU MCU Eclipse Plugin Content.xml Missing](GNU_MCU_Eclipse_Plugin_Content_XML_Missing.jpg)

Therefore, we have this Eclipse Plugin installed from within Eclipse MarketPlace as follows:

![GNU MCU Eclipse Marketplace](GNU_MCU_Eclipse_MarketPlace.jpg)


#### B. Install ARM Toolchain

It's clearly summarized in [https://gnu-mcu-eclipse.github.io/toolchain/arm/install/](https://gnu-mcu-eclipse.github.io/toolchain/arm/install/) that there are 2 ways to carry out the installation for GNU MCU Eclipse ARM Embedded GCC: **The xPack install** and **Manual install**.

**The manual install** is strongly recommended. You **ONLY** need to visit [GNU MCU Eclipse ARM Embedded GCC](https://github.com/gnu-mcu-eclipse/arm-none-eabi-gcc/releases), and download the corresponding file. [gnu-mcu-eclipse-arm-none-eabi-gcc-7.2.2-1.1-20180401-0515-centos64.tgz](https://github.com/gnu-mcu-eclipse/arm-none-eabi-gcc/releases/download/v7.2.2-1.1/gnu-mcu-eclipse-arm-none-eabi-gcc-7.2.2-1.1-20180401-0515-centos64.tgz) is downloaded and extracted under **/opt/GCCToolChains** in our case. Let's have a look at what files are under the ARM toolchain folder:

```
/opt/GCCToolChains/gnu-mcu-eclipse/arm-none-eabi-gcc/7.2.2-1.1-20180401-0515/bin$ ls
arm-none-eabi-addr2line  arm-none-eabi-elfedit    arm-none-eabi-gcc-ranlib  arm-none-eabi-gprof    arm-none-eabi-ranlib
arm-none-eabi-ar         arm-none-eabi-g++        arm-none-eabi-gcov        arm-none-eabi-ld       arm-none-eabi-readelf
arm-none-eabi-as         arm-none-eabi-gcc        arm-none-eabi-gcov-dump   arm-none-eabi-ld.bfd   arm-none-eabi-size
arm-none-eabi-c++        arm-none-eabi-gcc-7.2.2  arm-none-eabi-gcov-tool   arm-none-eabi-nm       arm-none-eabi-strings
arm-none-eabi-c++filt    arm-none-eabi-gcc-ar     arm-none-eabi-gdb         arm-none-eabi-objcopy  arm-none-eabi-strip
arm-none-eabi-cpp        arm-none-eabi-gcc-nm     arm-none-eabi-gdb-py      arm-none-eabi-objdump
```


#### C. Install J-Link

The J-Link binaries are available at [SEGGER](http://www.segger.com/jlink-software.html). In our case, **DEB installer 64-bit** is to be downloaded from [https://www.segger.com/downloads/jlink/JLink_Linux_x86_64.deb](https://www.segger.com/downloads/jlink/JLink_Linux_x86_64.deb). And to install it, we **ONLY** need to double-click this **deb** file under Ubuntu.


#### D. Install ST-Link

The reason why we need to install [ST-Link](https://github.com/texane/stlink) is that [Nucleo-144 board with STM32F767ZI](../../Part1_Introduction/01_Getting_Started_with_STM32/02_Nucleo-144_STM32F767ZI.md) comes with a ST-Link on board. The processes on how to checkout and build the source code are clearly displayed by the following commands:
```
$ git clone git@github.com:jiapei100/stlink.git
$ cd stlink
$ mkdir build
$ cd build
$ ccmake ../
$ make -j8
$ sudo checkinstall --fstrans=no
```

Four **exe** files are respectively installed as:
* /usr/local/bin/st-flash
* /usr/local/bin/st-info
* /usr/local/bin/st-util
* /usr/local/bin/stlink-gui


### Step 3: Workspace Preference

Finally, we enable **save automatically before build** and **UTF-8** encoding within **Workspace Preference**.

![Configuration in Workspace Preference](workspace_preference.jpg)


## 2.2.2 SW4STM32 (System Workbench for STM32)

To install the free IDE [System Workbench for STM32](http://www.st.com/en/development-tools/sw4stm32.html), [ST's official website](http://www.st.com/en/development-tools/sw4stm32.html) is redirected to [OpenSTM32](http://www.openstm32.org/). Users must first register on [OpenSTM32](http://www.openstm32.org/), and then strictly follow [Installing System Workbench for STM32](http://www.openstm32.org/Installing%2BSystem%2BWorkbench%2Bfor%2BSTM32).

Since we are going to use [2.2.1 GNU MCU Eclipse](https://gnu-mcu-eclipse.github.io/) throughout our course, we are **NOT** going to elaborate how to carry out the development for STM32 using [System Workbench for STM32](http://www.st.com/en/development-tools/sw4stm32.html).

