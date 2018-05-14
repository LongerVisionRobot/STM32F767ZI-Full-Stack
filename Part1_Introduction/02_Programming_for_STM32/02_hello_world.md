# 2.2 FIRST STM32 Project - "Hello World"

As any other programming languages, our first STM32 Project is also "Hello World", without hardware wiring. Using GNU MCU Eclipse to develop STM32 follows the same way to develop any other projects under Eclipse.


## Create an Project Under Eclipse

### Step 1: Steps To Create an Project

#### A. Create an Empty Project

**File**->**New**->**C/C++ Project**, then click on **C++ Managed Build**:

![Eclipse New Projects](./Eclipse_01_New_Projects.jpg)

Then, click **Next**.


#### B. Select STM32F7XX C/C++ Project

In the dialog **C++ Project**,
* under **Project type:**->**Executable**, select **STM32F7XX C/C++ Project**
* under **Project name:**, input **Hello World**

![Eclipse Create STM32FXX Projects](./Eclipse_02_New_Projects_STM32F7XX.jpg)

Then, click **Next**.


#### C. Target Processor Settings

In the dialog **Target Processor Settings**， 
* under **Chip family**, select **STM32F767xx**
* under **Flash size (kB):**, make sure it's **2048**
* under **External clock (Hz):"**, make sure it's **8000000**
* under **Content:**, select **Empty (add your own content)**
* under **Use system calls:**, select **Freestanding (no POSIX system calls)**

![Eclipse Target Processor Settings](Eclipse_03_Target_Processor_Settings.jpg)

Then, click **Next**.


#### D. Folder settings

![Eclipse Folders Settings](Eclipse_04_Folders_Settings.jpg)

Just click **Next**.


#### E. Select Configurations

![Eclipse Select Configurations](Eclipse_05_Select_Configurations.jpg)

Just click **Next**.


#### F. GNU ARM Cross Toolchain

![Eclipse GNU ARM Cross Toolchain](Eclipse_06_GNU_ARM_Cross_Toolchain.jpg)

Finally, click **Finish**.



## FIRST STM32 Project - "Hello World"

In Arduino IDe, to compile the above codes, click **Sketch->Verify/Compile**; to upload the code onto Arduino board afterwards, click **Sketch->Upload**.


![Eclipse Built Failure](Eclipse_07_Built_Failure.jpg)


![Eclipse Successfully Built](Eclipse_08_Successfully_Built.jpg)


![--specs=nosys.specs](Project_Properties_C++Build_Settings_ToolSettings_Linker_Miscellaneous.jpg)


