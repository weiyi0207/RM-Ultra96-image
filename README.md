# RM-Ultra96-image

This repository contains the boot files and runtime library for RoboRTS running on Ultra96.

## How to use

To run the RoboRTS on Ultra96, users need to boot the Ultra96 with dedicated boot files, which contains the necessary kernel driver and hardware accelerated functions' bitstream. 

Users need to copy the boot files in *Bootfiles* folder to Ultra96's SD card fat32 partition. The root file system for this project is recommended to use [PYNQ](http://www.pynq.io/home.html), which is based on Ubuntu 18.04 and compatible with ROS Melodic. 

**Users can download PYNQ Rootfs** in [PYNQ Image](http://www.pynq.io/board.html)

## Directory structure

File name | Description
--|--
Bootfiles | Boot files for Ultra96
Bootfiles/BOOT.BIN | FSBL, Bitstream, ATF, PMUFW, Uboot to boot Ultra96
Bootfiles/Image | Linux kernel image(Version 4.14) for Ultra96
Bootfiles/system.dtb | Linux device tree blob contains DPU information
misc/libdpumodelyolo.so | yolo model compiled as Shared library, users should place the model under */usr/lib*
misc/yolo.prototxt      | yolo model configuration file, users should place it under */etc/XILINX_AI_SDK.conf.d/*
