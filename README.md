# Shamu-kali
this is kernel source for nexus 6 (shamu)

include wireless firmware patch & hid interface patch
include toolchain

* for build stock kernel use the shamu_defconfig

* for Nethunter use kali_defconfig

<b> if you are lazy for compiling or you not have a PC you can download the kernel file from here [Shamu-kali/nigthly](https://github.com/JLynx69/Shamu-kali/tree/master/nightly) this file can install from your own TWRP</b>

kali_defconfig file in this directory /arch/arm/configs/

for kernel already modified just download from here [zImage-dtb](https://github.com/JLynx69/Shamu-kali/tree/master/device/moto/shamu-kernel) and for installation just following tutorial in README

for modifyng your own shamu kernel just following the command :

# NOTE : This require pc installed linux i368 or amd64 (recommended ubuntu 16.04 amd64)

clone this repository using: 

* git clone https://github.com/JLynx69/Shamu-kali.git

after done type this :
* sudo rm arch/arm/configs/kali_defconfig
* cd Shamu-kali
* export ARCH=arm
* export SUBARCH=arm
* export CROSS_COMPILE=`pwd`/toolchain/bin/arm-eabi-
* make shamu_defconfig
* make menuconfig
after this step you will activate or deactive kernel feature, for more klik here <b> [COMING SOON] </b>

after all done you will found a hidden file that name are .config
you just copy that file like this

* cp .config arch/arm/configs/kali_defconfig
after that start the building

* make O=../output kali_defconfig
* make O=../output -j4
in this step you will waiting for long time, in my time is 2 hours
because my computer is so poor just have 2 core of cpu :V

after everything are done you will found zImage, zImage-dtb on <b> arch/arm/boot/ </b>

that's kernel file can you flash on your nexus 6 devices

for tutorial how to flash your own modifying kernel klik here <b> [COMING SOON] </b>

sorry for my bad english :)
