![HeliOS](/profile/HeliOS_OG_Logo.png)
# Welcome
The HeliOS Project is an open source, community based, project to build and maintain a full-featured embedded operating system that meets the needs of academia, research, STEM education and enthusiasts alike. The HeliOS Project community represents a wide range of users and contributors from the electronics hobbyist implementing an embedded operating system in his/her Arduino project to a research scientist developing a remote sensing instrument that will be deployed to the field. Whether you wish to be a user or contributor, you are a part of the HeliOS Project community and for that we say welcome!
# Getting Started
## Arduino IDE

Using the HeliOS embedded operating system in your Arduino sketch could not be easier. Open the Arduino IDE and use the Library Manager to search for and install HeliOS. The folks at Arduino have the steps to install a library [here](https://docs.arduino.cc/software/ide-v1/tutorials/installing-libraries). Once installed, you can experiment with the example sketches that are included with HeliOS. Additional information about HeliOS and its syscalls can be found in the HeliOS Developer’s Guide [here](https://github.com/heliosproj/HeliOS/blob/master/doc/HeliOS_Developers_Guide.pdf).

## PlatformIO

HeliOS is also available through the PlatformIO registry and can be added to your project either through the PlatformIO IDE or CLI. The steps for which are described in the PlatformIO documentation [here](https://docs.platformio.org/en/latest/librarymanager/index.html). Like the Arduino IDE, several examples are included with HeliOS for you to experiment with. Additional information about HeliOS and its syscalls can be found in the HeliOS Developer’s Guide [here](https://github.com/heliosproj/HeliOS/blob/master/doc/HeliOS_Developers_Guide.pdf).

## ARM Cortex-M

If you are developing for the ARM Cortex-M series of processors, HeliOS includes full CMSIS support and can be easily integrated into your Keil uVision or vendor IDE project by:

1. Downloading the current release [here](https://github.com/heliosproj/HeliOS/releases) and unpacking the ZIP file into your project’s source directory
2. Downloading the CMSIS headers and vendor’s HAL/BSP headers and placing them into your project’s include directory
3. Adding the vendor’s HAL/BSP header to the HeliOS [port.h](https://github.com/heliosproj/HeliOS/blob/master/src/port.h) header immediately following the ``#elif defined(CMSIS_ARCH_CORTEXM)`` statement (i.e., line 52)
4. Setting ``SYSTEM_CORE_CLOCK_FREQUENCY`` and ``SYSTEM_CORE_CLOCK_PRESCALER`` in HeliOS’s [config.h](https://github.com/heliosproj/HeliOS/blob/master/src/config.h) header to match the Cortex-M’s core clock frequency and your desired prescaler
5. Add the ``-DCMSIS_ARCH_CORTEXM`` compiler directive to your project’s build configuration

Detailed information about HeliOS and its syscalls can be found in the HeliOS Developer’s Guide [here](https://github.com/heliosproj/HeliOS/blob/master/doc/HeliOS_Developers_Guide.pdf).
