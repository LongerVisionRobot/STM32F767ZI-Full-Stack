# 2.5 Test On Nucleo-144 STM32F767ZI

Finally, we come to test out some examples on board [Nucleo-144 STM32F767ZI](http://www.st.com/en/evaluation-tools/nucleo-f767zi.html).


## 2.5.1 Plug in Nucleo-144 STM32F767ZI

We first plug in the board [Nucleo-144 STM32F767ZI](http://www.st.com/en/evaluation-tools/nucleo-f767zi.html) as follows:

![STM32F767ZI STLink - 2 USB Ports](STM32F767ZI_STLink_2USB.jpg)

* On one side, plugging in the STLink USB port with the host computer is demonstrated by command **lsusb**.

```
$ lsusb
...
Bus 001 Device 005: ID 0483:374b STMicroelectronics ST-LINK/V2.1 (Nucleo-F103RB)
...
```
* On the other side, plugging in the other USB port for [Nucleo-144 STM32F767ZI](http://www.st.com/en/evaluation-tools/nucleo-f767zi.html) will be demonstrated by our test code.


## 2.5.2 Create and Build Project

Similar to [previous section](../02_Programming_for_STM32/04_QEMU_Simulation.md), this time, we create a **Blinky** C/C++ project with board configuration **STM32F7xx** with Chip family **STM32F767xx**. And we can also have the project successfully built with **Release** configuration with the following output:

```
17:57:31 **** Build of configuration Release for project F767ZI_Blinky ****
make all 
Building file: ../system/src/stm32f7-hal/stm32f7xx_hal.c
Invoking: GNU ARM Cross C Compiler
arm-none-eabi-gcc -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -DOS_USE_SEMIHOSTING -DNDEBUG -DSTM32F767xx -DUSE_HAL_DRIVER -DHSE_VALUE=8000000 -I"../include" -I"../system/include" -I"../system/include/cmsis" -I"../system/include/stm32f7-hal" -std=gnu11 -Wno-bad-function-cast -Wno-conversion -Wno-sign-conversion -Wno-unused-parameter -Wno-sign-compare -Wno-missing-prototypes -Wno-missing-declarations -MMD -MP -MF"system/src/stm32f7-hal/stm32f7xx_hal.d" -MT"system/src/stm32f7-hal/stm32f7xx_hal.o" -c -o "system/src/stm32f7-hal/stm32f7xx_hal.o" "../system/src/stm32f7-hal/stm32f7xx_hal.c"
Finished building: ../system/src/stm32f7-hal/stm32f7xx_hal.c
 
Building file: ../system/src/stm32f7-hal/stm32f7xx_hal_cortex.c
Invoking: GNU ARM Cross C Compiler
arm-none-eabi-gcc -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -DOS_USE_SEMIHOSTING -DNDEBUG -DSTM32F767xx -DUSE_HAL_DRIVER -DHSE_VALUE=8000000 -I"../include" -I"../system/include" -I"../system/include/cmsis" -I"../system/include/stm32f7-hal" -std=gnu11 -Wno-bad-function-cast -Wno-conversion -Wno-sign-conversion -Wno-unused-parameter -Wno-sign-compare -Wno-missing-prototypes -Wno-missing-declarations -MMD -MP -MF"system/src/stm32f7-hal/stm32f7xx_hal_cortex.d" -MT"system/src/stm32f7-hal/stm32f7xx_hal_cortex.o" -c -o "system/src/stm32f7-hal/stm32f7xx_hal_cortex.o" "../system/src/stm32f7-hal/stm32f7xx_hal_cortex.c"
Finished building: ../system/src/stm32f7-hal/stm32f7xx_hal_cortex.c
 
Building file: ../system/src/stm32f7-hal/stm32f7xx_hal_crc_ex.c
Invoking: GNU ARM Cross C Compiler
arm-none-eabi-gcc -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -DOS_USE_SEMIHOSTING -DNDEBUG -DSTM32F767xx -DUSE_HAL_DRIVER -DHSE_VALUE=8000000 -I"../include" -I"../system/include" -I"../system/include/cmsis" -I"../system/include/stm32f7-hal" -std=gnu11 -Wno-bad-function-cast -Wno-conversion -Wno-sign-conversion -Wno-unused-parameter -Wno-sign-compare -Wno-missing-prototypes -Wno-missing-declarations -MMD -MP -MF"system/src/stm32f7-hal/stm32f7xx_hal_crc_ex.d" -MT"system/src/stm32f7-hal/stm32f7xx_hal_crc_ex.o" -c -o "system/src/stm32f7-hal/stm32f7xx_hal_crc_ex.o" "../system/src/stm32f7-hal/stm32f7xx_hal_crc_ex.c"
Finished building: ../system/src/stm32f7-hal/stm32f7xx_hal_crc_ex.c
 
Building file: ../system/src/stm32f7-hal/stm32f7xx_hal_dfsdm.c
Invoking: GNU ARM Cross C Compiler
arm-none-eabi-gcc -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -DOS_USE_SEMIHOSTING -DNDEBUG -DSTM32F767xx -DUSE_HAL_DRIVER -DHSE_VALUE=8000000 -I"../include" -I"../system/include" -I"../system/include/cmsis" -I"../system/include/stm32f7-hal" -std=gnu11 -Wno-bad-function-cast -Wno-conversion -Wno-sign-conversion -Wno-unused-parameter -Wno-sign-compare -Wno-missing-prototypes -Wno-missing-declarations -MMD -MP -MF"system/src/stm32f7-hal/stm32f7xx_hal_dfsdm.d" -MT"system/src/stm32f7-hal/stm32f7xx_hal_dfsdm.o" -c -o "system/src/stm32f7-hal/stm32f7xx_hal_dfsdm.o" "../system/src/stm32f7-hal/stm32f7xx_hal_dfsdm.c"
Finished building: ../system/src/stm32f7-hal/stm32f7xx_hal_dfsdm.c
 
Building file: ../system/src/stm32f7-hal/stm32f7xx_hal_flash.c
Invoking: GNU ARM Cross C Compiler
arm-none-eabi-gcc -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -DOS_USE_SEMIHOSTING -DNDEBUG -DSTM32F767xx -DUSE_HAL_DRIVER -DHSE_VALUE=8000000 -I"../include" -I"../system/include" -I"../system/include/cmsis" -I"../system/include/stm32f7-hal" -std=gnu11 -Wno-bad-function-cast -Wno-conversion -Wno-sign-conversion -Wno-unused-parameter -Wno-sign-compare -Wno-missing-prototypes -Wno-missing-declarations -MMD -MP -MF"system/src/stm32f7-hal/stm32f7xx_hal_flash.d" -MT"system/src/stm32f7-hal/stm32f7xx_hal_flash.o" -c -o "system/src/stm32f7-hal/stm32f7xx_hal_flash.o" "../system/src/stm32f7-hal/stm32f7xx_hal_flash.c"
Finished building: ../system/src/stm32f7-hal/stm32f7xx_hal_flash.c
 
Building file: ../system/src/stm32f7-hal/stm32f7xx_hal_gpio.c
Invoking: GNU ARM Cross C Compiler
arm-none-eabi-gcc -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -DOS_USE_SEMIHOSTING -DNDEBUG -DSTM32F767xx -DUSE_HAL_DRIVER -DHSE_VALUE=8000000 -I"../include" -I"../system/include" -I"../system/include/cmsis" -I"../system/include/stm32f7-hal" -std=gnu11 -Wno-bad-function-cast -Wno-conversion -Wno-sign-conversion -Wno-unused-parameter -Wno-sign-compare -Wno-missing-prototypes -Wno-missing-declarations -MMD -MP -MF"system/src/stm32f7-hal/stm32f7xx_hal_gpio.d" -MT"system/src/stm32f7-hal/stm32f7xx_hal_gpio.o" -c -o "system/src/stm32f7-hal/stm32f7xx_hal_gpio.o" "../system/src/stm32f7-hal/stm32f7xx_hal_gpio.c"
Finished building: ../system/src/stm32f7-hal/stm32f7xx_hal_gpio.c
 
Building file: ../system/src/stm32f7-hal/stm32f7xx_hal_iwdg.c
Invoking: GNU ARM Cross C Compiler
arm-none-eabi-gcc -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -DOS_USE_SEMIHOSTING -DNDEBUG -DSTM32F767xx -DUSE_HAL_DRIVER -DHSE_VALUE=8000000 -I"../include" -I"../system/include" -I"../system/include/cmsis" -I"../system/include/stm32f7-hal" -std=gnu11 -Wno-bad-function-cast -Wno-conversion -Wno-sign-conversion -Wno-unused-parameter -Wno-sign-compare -Wno-missing-prototypes -Wno-missing-declarations -MMD -MP -MF"system/src/stm32f7-hal/stm32f7xx_hal_iwdg.d" -MT"system/src/stm32f7-hal/stm32f7xx_hal_iwdg.o" -c -o "system/src/stm32f7-hal/stm32f7xx_hal_iwdg.o" "../system/src/stm32f7-hal/stm32f7xx_hal_iwdg.c"
Finished building: ../system/src/stm32f7-hal/stm32f7xx_hal_iwdg.c
 
Building file: ../system/src/stm32f7-hal/stm32f7xx_hal_jpeg.c
Invoking: GNU ARM Cross C Compiler
arm-none-eabi-gcc -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -DOS_USE_SEMIHOSTING -DNDEBUG -DSTM32F767xx -DUSE_HAL_DRIVER -DHSE_VALUE=8000000 -I"../include" -I"../system/include" -I"../system/include/cmsis" -I"../system/include/stm32f7-hal" -std=gnu11 -Wno-bad-function-cast -Wno-conversion -Wno-sign-conversion -Wno-unused-parameter -Wno-sign-compare -Wno-missing-prototypes -Wno-missing-declarations -MMD -MP -MF"system/src/stm32f7-hal/stm32f7xx_hal_jpeg.d" -MT"system/src/stm32f7-hal/stm32f7xx_hal_jpeg.o" -c -o "system/src/stm32f7-hal/stm32f7xx_hal_jpeg.o" "../system/src/stm32f7-hal/stm32f7xx_hal_jpeg.c"
Finished building: ../system/src/stm32f7-hal/stm32f7xx_hal_jpeg.c
 
Building file: ../system/src/stm32f7-hal/stm32f7xx_hal_mdios.c
Invoking: GNU ARM Cross C Compiler
arm-none-eabi-gcc -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -DOS_USE_SEMIHOSTING -DNDEBUG -DSTM32F767xx -DUSE_HAL_DRIVER -DHSE_VALUE=8000000 -I"../include" -I"../system/include" -I"../system/include/cmsis" -I"../system/include/stm32f7-hal" -std=gnu11 -Wno-bad-function-cast -Wno-conversion -Wno-sign-conversion -Wno-unused-parameter -Wno-sign-compare -Wno-missing-prototypes -Wno-missing-declarations -MMD -MP -MF"system/src/stm32f7-hal/stm32f7xx_hal_mdios.d" -MT"system/src/stm32f7-hal/stm32f7xx_hal_mdios.o" -c -o "system/src/stm32f7-hal/stm32f7xx_hal_mdios.o" "../system/src/stm32f7-hal/stm32f7xx_hal_mdios.c"
Finished building: ../system/src/stm32f7-hal/stm32f7xx_hal_mdios.c
 
Building file: ../system/src/stm32f7-hal/stm32f7xx_hal_pwr.c
Invoking: GNU ARM Cross C Compiler
arm-none-eabi-gcc -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -DOS_USE_SEMIHOSTING -DNDEBUG -DSTM32F767xx -DUSE_HAL_DRIVER -DHSE_VALUE=8000000 -I"../include" -I"../system/include" -I"../system/include/cmsis" -I"../system/include/stm32f7-hal" -std=gnu11 -Wno-bad-function-cast -Wno-conversion -Wno-sign-conversion -Wno-unused-parameter -Wno-sign-compare -Wno-missing-prototypes -Wno-missing-declarations -MMD -MP -MF"system/src/stm32f7-hal/stm32f7xx_hal_pwr.d" -MT"system/src/stm32f7-hal/stm32f7xx_hal_pwr.o" -c -o "system/src/stm32f7-hal/stm32f7xx_hal_pwr.o" "../system/src/stm32f7-hal/stm32f7xx_hal_pwr.c"
Finished building: ../system/src/stm32f7-hal/stm32f7xx_hal_pwr.c
 
Building file: ../system/src/stm32f7-hal/stm32f7xx_hal_pwr_ex.c
Invoking: GNU ARM Cross C Compiler
arm-none-eabi-gcc -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -DOS_USE_SEMIHOSTING -DNDEBUG -DSTM32F767xx -DUSE_HAL_DRIVER -DHSE_VALUE=8000000 -I"../include" -I"../system/include" -I"../system/include/cmsis" -I"../system/include/stm32f7-hal" -std=gnu11 -Wno-bad-function-cast -Wno-conversion -Wno-sign-conversion -Wno-unused-parameter -Wno-sign-compare -Wno-missing-prototypes -Wno-missing-declarations -MMD -MP -MF"system/src/stm32f7-hal/stm32f7xx_hal_pwr_ex.d" -MT"system/src/stm32f7-hal/stm32f7xx_hal_pwr_ex.o" -c -o "system/src/stm32f7-hal/stm32f7xx_hal_pwr_ex.o" "../system/src/stm32f7-hal/stm32f7xx_hal_pwr_ex.c"
Finished building: ../system/src/stm32f7-hal/stm32f7xx_hal_pwr_ex.c
 
Building file: ../system/src/stm32f7-hal/stm32f7xx_hal_rcc.c
Invoking: GNU ARM Cross C Compiler
arm-none-eabi-gcc -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -DOS_USE_SEMIHOSTING -DNDEBUG -DSTM32F767xx -DUSE_HAL_DRIVER -DHSE_VALUE=8000000 -I"../include" -I"../system/include" -I"../system/include/cmsis" -I"../system/include/stm32f7-hal" -std=gnu11 -Wno-bad-function-cast -Wno-conversion -Wno-sign-conversion -Wno-unused-parameter -Wno-sign-compare -Wno-missing-prototypes -Wno-missing-declarations -MMD -MP -MF"system/src/stm32f7-hal/stm32f7xx_hal_rcc.d" -MT"system/src/stm32f7-hal/stm32f7xx_hal_rcc.o" -c -o "system/src/stm32f7-hal/stm32f7xx_hal_rcc.o" "../system/src/stm32f7-hal/stm32f7xx_hal_rcc.c"
Finished building: ../system/src/stm32f7-hal/stm32f7xx_hal_rcc.c
 
Building file: ../system/src/stm32f7-hal/stm32f7xx_hal_rcc_ex.c
Invoking: GNU ARM Cross C Compiler
arm-none-eabi-gcc -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -DOS_USE_SEMIHOSTING -DNDEBUG -DSTM32F767xx -DUSE_HAL_DRIVER -DHSE_VALUE=8000000 -I"../include" -I"../system/include" -I"../system/include/cmsis" -I"../system/include/stm32f7-hal" -std=gnu11 -Wno-bad-function-cast -Wno-conversion -Wno-sign-conversion -Wno-unused-parameter -Wno-sign-compare -Wno-missing-prototypes -Wno-missing-declarations -MMD -MP -MF"system/src/stm32f7-hal/stm32f7xx_hal_rcc_ex.d" -MT"system/src/stm32f7-hal/stm32f7xx_hal_rcc_ex.o" -c -o "system/src/stm32f7-hal/stm32f7xx_hal_rcc_ex.o" "../system/src/stm32f7-hal/stm32f7xx_hal_rcc_ex.c"
Finished building: ../system/src/stm32f7-hal/stm32f7xx_hal_rcc_ex.c
 
Building file: ../system/src/stm32f7-hal/stm32f7xx_hal_smartcard_ex.c
Invoking: GNU ARM Cross C Compiler
arm-none-eabi-gcc -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -DOS_USE_SEMIHOSTING -DNDEBUG -DSTM32F767xx -DUSE_HAL_DRIVER -DHSE_VALUE=8000000 -I"../include" -I"../system/include" -I"../system/include/cmsis" -I"../system/include/stm32f7-hal" -std=gnu11 -Wno-bad-function-cast -Wno-conversion -Wno-sign-conversion -Wno-unused-parameter -Wno-sign-compare -Wno-missing-prototypes -Wno-missing-declarations -MMD -MP -MF"system/src/stm32f7-hal/stm32f7xx_hal_smartcard_ex.d" -MT"system/src/stm32f7-hal/stm32f7xx_hal_smartcard_ex.o" -c -o "system/src/stm32f7-hal/stm32f7xx_hal_smartcard_ex.o" "../system/src/stm32f7-hal/stm32f7xx_hal_smartcard_ex.c"
Finished building: ../system/src/stm32f7-hal/stm32f7xx_hal_smartcard_ex.c
 
Building file: ../system/src/newlib/_cxx.cpp
Invoking: GNU ARM Cross C++ Compiler
arm-none-eabi-g++ -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -DOS_USE_SEMIHOSTING -DNDEBUG -DSTM32F767xx -DUSE_HAL_DRIVER -DHSE_VALUE=8000000 -I"../include" -I"../system/include" -I"../system/include/cmsis" -I"../system/include/stm32f7-hal" -std=gnu++11 -fabi-version=0 -fno-exceptions -fno-rtti -fno-use-cxa-atexit -fno-threadsafe-statics -MMD -MP -MF"system/src/newlib/_cxx.d" -MT"system/src/newlib/_cxx.o" -c -o "system/src/newlib/_cxx.o" "../system/src/newlib/_cxx.cpp"
Finished building: ../system/src/newlib/_cxx.cpp
 
Building file: ../system/src/newlib/_exit.c
Invoking: GNU ARM Cross C Compiler
arm-none-eabi-gcc -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -DOS_USE_SEMIHOSTING -DNDEBUG -DSTM32F767xx -DUSE_HAL_DRIVER -DHSE_VALUE=8000000 -I"../include" -I"../system/include" -I"../system/include/cmsis" -I"../system/include/stm32f7-hal" -std=gnu11 -MMD -MP -MF"system/src/newlib/_exit.d" -MT"system/src/newlib/_exit.o" -c -o "system/src/newlib/_exit.o" "../system/src/newlib/_exit.c"
Finished building: ../system/src/newlib/_exit.c
 
Building file: ../system/src/newlib/_sbrk.c
Invoking: GNU ARM Cross C Compiler
arm-none-eabi-gcc -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -DOS_USE_SEMIHOSTING -DNDEBUG -DSTM32F767xx -DUSE_HAL_DRIVER -DHSE_VALUE=8000000 -I"../include" -I"../system/include" -I"../system/include/cmsis" -I"../system/include/stm32f7-hal" -std=gnu11 -MMD -MP -MF"system/src/newlib/_sbrk.d" -MT"system/src/newlib/_sbrk.o" -c -o "system/src/newlib/_sbrk.o" "../system/src/newlib/_sbrk.c"
Finished building: ../system/src/newlib/_sbrk.c
 
Building file: ../system/src/newlib/_startup.c
Invoking: GNU ARM Cross C Compiler
arm-none-eabi-gcc -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -DOS_USE_SEMIHOSTING -DNDEBUG -DSTM32F767xx -DUSE_HAL_DRIVER -DHSE_VALUE=8000000 -DOS_INCLUDE_STARTUP_INIT_MULTIPLE_RAM_SECTIONS -I"../include" -I"../system/include" -I"../system/include/cmsis" -I"../system/include/stm32f7-hal" -std=gnu11 -MMD -MP -MF"system/src/newlib/_startup.d" -MT"system/src/newlib/_startup.d" -c -o "system/src/newlib/_startup.o" "../system/src/newlib/_startup.c"
Finished building: ../system/src/newlib/_startup.c
 
Building file: ../system/src/newlib/_syscalls.c
Invoking: GNU ARM Cross C Compiler
arm-none-eabi-gcc -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -DOS_USE_SEMIHOSTING -DNDEBUG -DSTM32F767xx -DUSE_HAL_DRIVER -DHSE_VALUE=8000000 -I"../include" -I"../system/include" -I"../system/include/cmsis" -I"../system/include/stm32f7-hal" -std=gnu11 -MMD -MP -MF"system/src/newlib/_syscalls.d" -MT"system/src/newlib/_syscalls.o" -c -o "system/src/newlib/_syscalls.o" "../system/src/newlib/_syscalls.c"
Finished building: ../system/src/newlib/_syscalls.c
 
Building file: ../system/src/newlib/assert.c
Invoking: GNU ARM Cross C Compiler
arm-none-eabi-gcc -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -DOS_USE_SEMIHOSTING -DNDEBUG -DSTM32F767xx -DUSE_HAL_DRIVER -DHSE_VALUE=8000000 -I"../include" -I"../system/include" -I"../system/include/cmsis" -I"../system/include/stm32f7-hal" -std=gnu11 -MMD -MP -MF"system/src/newlib/assert.d" -MT"system/src/newlib/assert.o" -c -o "system/src/newlib/assert.o" "../system/src/newlib/assert.c"
Finished building: ../system/src/newlib/assert.c
 
Building file: ../system/src/diag/Trace.c
Invoking: GNU ARM Cross C Compiler
arm-none-eabi-gcc -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -DOS_USE_SEMIHOSTING -DNDEBUG -DSTM32F767xx -DUSE_HAL_DRIVER -DHSE_VALUE=8000000 -I"../include" -I"../system/include" -I"../system/include/cmsis" -I"../system/include/stm32f7-hal" -std=gnu11 -MMD -MP -MF"system/src/diag/Trace.d" -MT"system/src/diag/Trace.o" -c -o "system/src/diag/Trace.o" "../system/src/diag/Trace.c"
Finished building: ../system/src/diag/Trace.c
 
Building file: ../system/src/diag/trace_impl.c
Invoking: GNU ARM Cross C Compiler
arm-none-eabi-gcc -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -DOS_USE_SEMIHOSTING -DNDEBUG -DSTM32F767xx -DUSE_HAL_DRIVER -DHSE_VALUE=8000000 -I"../include" -I"../system/include" -I"../system/include/cmsis" -I"../system/include/stm32f7-hal" -std=gnu11 -MMD -MP -MF"system/src/diag/trace_impl.d" -MT"system/src/diag/trace_impl.o" -c -o "system/src/diag/trace_impl.o" "../system/src/diag/trace_impl.c"
Finished building: ../system/src/diag/trace_impl.c
 
Building file: ../system/src/cortexm/_initialize_hardware.c
Invoking: GNU ARM Cross C Compiler
arm-none-eabi-gcc -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -DOS_USE_SEMIHOSTING -DNDEBUG -DSTM32F767xx -DUSE_HAL_DRIVER -DHSE_VALUE=8000000 -I"../include" -I"../system/include" -I"../system/include/cmsis" -I"../system/include/stm32f7-hal" -std=gnu11 -MMD -MP -MF"system/src/cortexm/_initialize_hardware.d" -MT"system/src/cortexm/_initialize_hardware.o" -c -o "system/src/cortexm/_initialize_hardware.o" "../system/src/cortexm/_initialize_hardware.c"
Finished building: ../system/src/cortexm/_initialize_hardware.c
 
Building file: ../system/src/cortexm/_reset_hardware.c
Invoking: GNU ARM Cross C Compiler
arm-none-eabi-gcc -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -DOS_USE_SEMIHOSTING -DNDEBUG -DSTM32F767xx -DUSE_HAL_DRIVER -DHSE_VALUE=8000000 -I"../include" -I"../system/include" -I"../system/include/cmsis" -I"../system/include/stm32f7-hal" -std=gnu11 -MMD -MP -MF"system/src/cortexm/_reset_hardware.d" -MT"system/src/cortexm/_reset_hardware.o" -c -o "system/src/cortexm/_reset_hardware.o" "../system/src/cortexm/_reset_hardware.c"
Finished building: ../system/src/cortexm/_reset_hardware.c
 
Building file: ../system/src/cortexm/exception_handlers.c
Invoking: GNU ARM Cross C Compiler
arm-none-eabi-gcc -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -DOS_USE_SEMIHOSTING -DNDEBUG -DSTM32F767xx -DUSE_HAL_DRIVER -DHSE_VALUE=8000000 -I"../include" -I"../system/include" -I"../system/include/cmsis" -I"../system/include/stm32f7-hal" -std=gnu11 -MMD -MP -MF"system/src/cortexm/exception_handlers.d" -MT"system/src/cortexm/exception_handlers.o" -c -o "system/src/cortexm/exception_handlers.o" "../system/src/cortexm/exception_handlers.c"
Finished building: ../system/src/cortexm/exception_handlers.c
 
Building file: ../system/src/cmsis/system_stm32f7xx.c
Invoking: GNU ARM Cross C Compiler
arm-none-eabi-gcc -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -DOS_USE_SEMIHOSTING -DNDEBUG -DSTM32F767xx -DUSE_HAL_DRIVER -DHSE_VALUE=8000000 -I"../include" -I"../system/include" -I"../system/include/cmsis" -I"../system/include/stm32f7-hal" -std=gnu11 -MMD -MP -MF"system/src/cmsis/system_stm32f7xx.d" -MT"system/src/cmsis/system_stm32f7xx.o" -c -o "system/src/cmsis/system_stm32f7xx.o" "../system/src/cmsis/system_stm32f7xx.c"
Finished building: ../system/src/cmsis/system_stm32f7xx.c
 
Building file: ../system/src/cmsis/vectors_stm32f767xx.c
Invoking: GNU ARM Cross C Compiler
arm-none-eabi-gcc -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -DOS_USE_SEMIHOSTING -DNDEBUG -DSTM32F767xx -DUSE_HAL_DRIVER -DHSE_VALUE=8000000 -I"../include" -I"../system/include" -I"../system/include/cmsis" -I"../system/include/stm32f7-hal" -std=gnu11 -MMD -MP -MF"system/src/cmsis/vectors_stm32f767xx.d" -MT"system/src/cmsis/vectors_stm32f767xx.o" -c -o "system/src/cmsis/vectors_stm32f767xx.o" "../system/src/cmsis/vectors_stm32f767xx.c"
Finished building: ../system/src/cmsis/vectors_stm32f767xx.c
 
Building file: ../src/BlinkLed.cpp
Invoking: GNU ARM Cross C++ Compiler
arm-none-eabi-g++ -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -DOS_USE_SEMIHOSTING -DNDEBUG -DSTM32F767xx -DUSE_HAL_DRIVER -DHSE_VALUE=8000000 -I"../include" -I"../system/include" -I"../system/include/cmsis" -I"../system/include/stm32f7-hal" -std=gnu++11 -fabi-version=0 -fno-exceptions -fno-rtti -fno-use-cxa-atexit -fno-threadsafe-statics -MMD -MP -MF"src/BlinkLed.d" -MT"src/BlinkLed.o" -c -o "src/BlinkLed.o" "../src/BlinkLed.cpp"
Finished building: ../src/BlinkLed.cpp
 
Building file: ../src/Timer.cpp
Invoking: GNU ARM Cross C++ Compiler
arm-none-eabi-g++ -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -DOS_USE_SEMIHOSTING -DNDEBUG -DSTM32F767xx -DUSE_HAL_DRIVER -DHSE_VALUE=8000000 -I"../include" -I"../system/include" -I"../system/include/cmsis" -I"../system/include/stm32f7-hal" -std=gnu++11 -fabi-version=0 -fno-exceptions -fno-rtti -fno-use-cxa-atexit -fno-threadsafe-statics -MMD -MP -MF"src/Timer.d" -MT"src/Timer.o" -c -o "src/Timer.o" "../src/Timer.cpp"
Finished building: ../src/Timer.cpp
 
Building file: ../src/_initialize_hardware.c
Invoking: GNU ARM Cross C Compiler
arm-none-eabi-gcc -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -DOS_USE_SEMIHOSTING -DNDEBUG -DSTM32F767xx -DUSE_HAL_DRIVER -DHSE_VALUE=8000000 -I"../include" -I"../system/include" -I"../system/include/cmsis" -I"../system/include/stm32f7-hal" -std=gnu11 -MMD -MP -MF"src/_initialize_hardware.d" -MT"src/_initialize_hardware.o" -c -o "src/_initialize_hardware.o" "../src/_initialize_hardware.c"
../src/_initialize_hardware.c: In function 'SystemClock_Config':
../src/_initialize_hardware.c:150:2: warning: #warning "Please check if the SystemClock_Config() settings match your board!" [-Wcpp]
 #warning "Please check if the SystemClock_Config() settings match your board!"
  ^~~~~~~
Finished building: ../src/_initialize_hardware.c
 
Building file: ../src/_write.c
Invoking: GNU ARM Cross C Compiler
arm-none-eabi-gcc -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -DOS_USE_SEMIHOSTING -DNDEBUG -DSTM32F767xx -DUSE_HAL_DRIVER -DHSE_VALUE=8000000 -I"../include" -I"../system/include" -I"../system/include/cmsis" -I"../system/include/stm32f7-hal" -std=gnu11 -MMD -MP -MF"src/_write.d" -MT"src/_write.o" -c -o "src/_write.o" "../src/_write.c"
Finished building: ../src/_write.c
 
Building file: ../src/main.cpp
Invoking: GNU ARM Cross C++ Compiler
arm-none-eabi-g++ -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -DOS_USE_SEMIHOSTING -DNDEBUG -DSTM32F767xx -DUSE_HAL_DRIVER -DHSE_VALUE=8000000 -I"../include" -I"../system/include" -I"../system/include/cmsis" -I"../system/include/stm32f7-hal" -std=gnu++11 -fabi-version=0 -fno-exceptions -fno-rtti -fno-use-cxa-atexit -fno-threadsafe-statics -MMD -MP -MF"src/main.d" -MT"src/main.o" -c -o "src/main.o" "../src/main.cpp"
../src/main.cpp:113:2: warning: #warning "Unknown board, assume PA5, active high." [-Wcpp]
 #warning "Unknown board, assume PA5, active high."
  ^~~~~~~
Finished building: ../src/main.cpp
 
Building file: ../src/stm32f7xx_hal_msp.c
Invoking: GNU ARM Cross C Compiler
arm-none-eabi-gcc -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -DOS_USE_SEMIHOSTING -DNDEBUG -DSTM32F767xx -DUSE_HAL_DRIVER -DHSE_VALUE=8000000 -I"../include" -I"../system/include" -I"../system/include/cmsis" -I"../system/include/stm32f7-hal" -std=gnu11 -Wno-missing-prototypes -Wno-missing-declarations -MMD -MP -MF"src/stm32f7xx_hal_msp.d" -MT"src/stm32f7xx_hal_msp.d" -c -o "src/stm32f7xx_hal_msp.o" "../src/stm32f7xx_hal_msp.c"
Finished building: ../src/stm32f7xx_hal_msp.c
 
Building target: F767ZI_Blinky.elf
Invoking: GNU ARM Cross C++ Linker
arm-none-eabi-g++ -mcpu=cortex-m7 -mthumb -mfloat-abi=soft -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall -Wextra  -g -T mem.ld -T libs.ld -T sections.ld -nostartfiles -Xlinker --gc-sections -L"../ldscripts" -Wl,-Map,"F767ZI_Blinky.map" --specs=nano.specs -o "F767ZI_Blinky.elf"  ./system/src/stm32f7-hal/stm32f7xx_hal.o ./system/src/stm32f7-hal/stm32f7xx_hal_cortex.o ./system/src/stm32f7-hal/stm32f7xx_hal_crc_ex.o ./system/src/stm32f7-hal/stm32f7xx_hal_dfsdm.o ./system/src/stm32f7-hal/stm32f7xx_hal_flash.o ./system/src/stm32f7-hal/stm32f7xx_hal_gpio.o ./system/src/stm32f7-hal/stm32f7xx_hal_iwdg.o ./system/src/stm32f7-hal/stm32f7xx_hal_jpeg.o ./system/src/stm32f7-hal/stm32f7xx_hal_mdios.o ./system/src/stm32f7-hal/stm32f7xx_hal_pwr.o ./system/src/stm32f7-hal/stm32f7xx_hal_pwr_ex.o ./system/src/stm32f7-hal/stm32f7xx_hal_rcc.o ./system/src/stm32f7-hal/stm32f7xx_hal_rcc_ex.o ./system/src/stm32f7-hal/stm32f7xx_hal_smartcard_ex.o  ./system/src/newlib/_cxx.o ./system/src/newlib/_exit.o ./system/src/newlib/_sbrk.o ./system/src/newlib/_startup.o ./system/src/newlib/_syscalls.o ./system/src/newlib/assert.o  ./system/src/diag/Trace.o ./system/src/diag/trace_impl.o  ./system/src/cortexm/_initialize_hardware.o ./system/src/cortexm/_reset_hardware.o ./system/src/cortexm/exception_handlers.o  ./system/src/cmsis/system_stm32f7xx.o ./system/src/cmsis/vectors_stm32f767xx.o  ./src/BlinkLed.o ./src/Timer.o ./src/_initialize_hardware.o ./src/_write.o ./src/main.o ./src/stm32f7xx_hal_msp.o   
Finished building target: F767ZI_Blinky.elf
 
Invoking: GNU ARM Cross Create Flash Image
arm-none-eabi-objcopy -O ihex "F767ZI_Blinky.elf"  "F767ZI_Blinky.hex"
Finished building: F767ZI_Blinky.hex
 
Invoking: GNU ARM Cross Print Size
arm-none-eabi-size --format=berkeley "F767ZI_Blinky.elf"
   text	   data	    bss	    dec	    hex	filename
   8591	    512	    588	   9691	   25db	F767ZI_Blinky.elf
Finished building: F767ZI_Blinky.siz
 

17:57:34 Build Finished (took 3s.375ms)
```


## 2.5.3 Flash Built .elf onto Nucleo-144 STM32F767ZI


