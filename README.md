RK3576
-----------
[中文](./README_CN.md)
* [Product Introduction](#product-introduction)
* [User Guide](#user-guide)
* [Parameter Configuration](#parameter-configuration)
* [Resource Download](#resource-download)


# Product Introduction

**Overview of the Development Board**

This development board based on the RK3576 chip is a high-performance development platform specifically designed for developers and embedded system enthusiasts.It takes Rockchip's RK3576 chip as its core, integrates rich interfaces and practical modules, and can provide powerful and convenient hardware support for the development of various embedded projects.Whether it is the development of Internet of Things devices, the research and development of smart terminals, or the testing of multimedia applications and other scenarios, this development board can meet different development needs with its outstanding performance and flexible scalability, and help developers quickly advance the project progress.

![1](https://github.com/shiviz-dev/rk3576/blob/adjustment_directory/Documents/images/f241d26136e6f4af8af8289783006269.jpg)

**Core advantage**


The core advantage of this development board stems from the RK3576 chip it is equipped with.  This chip adopts an eight-core 64-bit design, integrating 4 Cortex-A72 cores and 4 Cortex-A53 cores.  Its powerful processing capability can easily handle complex computing tasks.  Meanwhile, it is equipped with an NPU with a built-in computing power of 6 TOPS, which can efficiently support the operation of artificial intelligence algorithms and endow the development board with outstanding AI processing capabilities.  In addition, the development board supports multiple operating systems such as Android 14 and Debian 12, significantly enhancing the flexibility and adaptability of development.

In terms of interface configuration, the development board is equipped with a rich variety of interfaces. The network port can provide a stable network connection, meeting the requirements for the development board to access the network for data interaction and remote control. The mipi csi 4lane interface can be connected to the camera, facilitating related developments such as image acquisition. The USB3.0 interface supports high-speed data transmission, facilitating the connection of external storage devices and other peripherals. The Tape-C interface has diverse functions, including data transmission and ADB debugging, etc. These interfaces expand the application scenarios of the development board and enable it to adapt to a variety of external devices.

In terms of module functionality, EMMC is responsible for the persistent storage of data and can reliably save the operating system, application programs and user data.  LPDDR4 provides a cache for CPU data processing, enhancing the speed and efficiency of data processing.  The wifi-bt-module supports wireless connection, enabling the development board to achieve wireless Internet access and wireless communication between devices, and enhancing its convenience of use in wireless scenarios.  All modules work in coordination to ensure the stable operation and functional realization of the development board, highlighting the advantages of the high-performance development platform.

# User Guide

**Burn the firmware**

****Step 1: Installation of Windows drivers****

(1) Open the software in the DriverAssitant folder, which is designed for the installation of development board drivers.

![2](https://github.com/shiviz-dev/rk3576/blob/adjustment_directory/Documents/images/2551f625c9584a9f228a7fabb5b53e94.jpg)

(2) Select the driver installation option, follow the software prompts step by step to complete the driver installation, and ensure that the development board can communicate normally with the computer.

![3](https://github.com/shiviz-dev/rk3576/blob/adjustment_directory/Documents/images/6a3acd2996ee609f44f0e70e7a7b7a78.jpg)

****Step 2: Enter the download mode****

(1) Method 1: Connect your computer to the type-c interface at the board end, hold down the BOOT button for a long time, then turn on the power. Wait for one or two seconds and release the BOOT button. At this point, the development board successfully enters the download mode.

![4](https://github.com/shiviz-dev/rk3576/blob/adjustment_directory/Documents/images/ca1f0a4fca70c4be22c16cbfc498c36c.jpg)

(2) Method 2: Use DEBUG or ADB to open the terminal and enter the command `reboot loader` to enter the download mode

****Step 3: Burn****

******Windows flashing******

(1) Open the RKDevTool software on the computer. If the bottom of the software shows "A LOADER device found", it indicates that the board has entered the download mode and subsequent burning operations can be carried out.

![5](https://github.com/shiviz-dev/rk3576/blob/adjustment_directory/Documents/images/665f35172233570bdf9825aefc33a39d.jpg)

(2) On the download image interface, developers can choose to burn a specific part of the image separately based on their actual needs, flexibly meeting different development scenarios.

![6](https://github.com/shiviz-dev/rk3576/blob/adjustment_directory/Documents/images/36729c52203d8c3d6b336c118b982f41.jpg)

(3) On the firmware upgrade interface, you can choose to burn the entire firmware to complete the system update or installation at one time.

![7](https://github.com/shiviz-dev/rk3576/blob/adjustment_directory/Documents/images/f023aadacca7fe22cb682e0ddec993c6.jpg)

(4) Wait for the burning to complete. During the burning process, please ensure a stable connection between the development board and the computer to avoid burning failure due to connection issues.

![8](https://github.com/shiviz-dev/rk3576/blob/adjustment_directory/Documents/images/32df832a964e33e1f5cf0abacb02afc2.jpg)

******Linux flashing******

Use the command: 
```bash 
sudo./upgrade_tool uf update.img
```

Among them, `update.img` is the system image to be burned


# Parameter Configuration

| 类别                | 详情                                                                 |
|---------------------|----------------------------------------------------------------------|
| 尺寸大小            | 61mm × 40mm × 9mm                                                    |
| 产品基础参数        | 瑞芯微RK3576开发板                                                   |
| 系统级芯片 (SoC)    | 瑞芯微RK3576                                                         |
| 中央处理器 (CPU)    | 4×Cortex - A72 + 4×Cortex - A53（大小核架构）                        |
| 图形处理器 (GPU)    | Arm Mali - G52 MC3                                                   |
| 神经网络加速器 (NPU) | 6TOPS（支持INT4/INT8/INT16/FP16/BF16/TF32）                          |
| 指令集架构 (ISA)    | ARMv8-A，含TrustZone和加密扩展                                        |
| 运行内存 (RAM)      | LPDDR4，4G                                                          |
| 存储（EMMC）        | 32G                                                                 |
| 无线连接            | AP6256，Wi-Fi5（802.11ac）、蓝牙 5.0（含BLE），外接天线接口           |
| **接口**            |                                                                      |
| MIPI CSI 接口       | 1路4lane（IMX566、IMX415、OV5640等）                                 |
| USB3.0              | 连接器（BTB Connector）                                              |
| Type-C              | 支持ADB、USB3.0                                                      |
| 有线以太网          | 1个千兆以太网口                                                       |
| UART                | 1×UART                                                               |
| DEBUG               | 用于开发调试                                                         |
| 电源输入            | 5V                                                                   |
| **软件**            |                                                                      |
| 操作系统            | 支持 Debian12、Android 14、Yocto、Buildroot                          |
| 开发工具包          | 支持 Rockchip RKNN SDK                                               |
| 模型框架兼容        | 支持 TensorFlow、PyTorch、ONNX，通过 RKNN 工具部署                     |
| 实际兼容模型        | 支持 DeepSeek1.5B（INT4）、RWKV、YOLOX、NanoDet等                    |


# Resource Download

****Document link****

[rk3576.doc](https://github.com/shiviz-dev/rk3576/blob/adjustment_directory/Documents/RK3576.doc)

[Download of image file](https://github.com/shiviz-dev/rk3576-dev-board/releases/)