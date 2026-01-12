RK3576
-----------
[English](./README.md)
* [产品介绍](#产品介绍)
* [用户指南](#用户指南)
* [参数配置](#参数配置)
* [资源下载](#资源下载)


# 产品介绍

**开发板概述**

基于 RK3576 芯片的这款开发板，是专为开发者和嵌入式系统爱好者打造的高性能开发平台。它以瑞芯微电子的 RK3576 芯片为核心，集成了丰富的接口和实用模块，能为各类嵌入式项目开发提供强大且便捷的硬件支持。无论是物联网设备开发、智能终端研发，还是多媒体应用测试等场景，该开发板都能凭借其出色的性能和灵活的扩展性，满足不同开发需求，助力开发者快速推进项目进程。

![1](https://github.com/shiviz-dev/rk3576/blob/adjustment_directory/Documents/images/f241d26136e6f4af8af8289783006269.jpg)

**核心优势**


该开发板的核心优势源于其搭载的 RK3576 芯片。此芯片采用八核心 64 位设计，融合 4 个 Cortex - A72 核心与 4 个 Cortex - A53 核心，强大的处理能力可轻松应对复杂的计算任务。同时，内置 6 TOPS 算力的 NPU，能高效支持人工智能算法运行，为开发板赋予出色的 AI 处理能力。此外，开发板支持 Android 14、Debian 12 等多种操作系统，大大提升了开发的灵活性和适配性。

在接口配置上，开发板配备了丰富多样的接口。网口能提供稳定的网络连接，满足开发板接入网络进行数据交互和远程控制的需求；mipi csi 4lane 接口可连接摄像头，便于开展图像采集等相关开发；USB3.0 接口支持高速数据传输，方便连接外部存储设备和其他外设；Tape - C 接口功能多样，兼顾数据传输和ADB调试等，这些接口为开发板拓展了丰富的应用场景，使其能适配多种外部设备。

在模块功能上，EMMC 负责数据的持久化存储，能可靠保存操作系统、应用程序和用户数据；LPDDR4 为 CPU 处理数据提供高速缓存，提升了数据处理速度和效率；wifi - bt - module 支持无线连接，让开发板能实现无线上网和设备间无线通信，增强了其在无线场景下的使用便利性。各模块协同工作，确保了开发板的稳定运行和功能实现，凸显高性能开发平台的优势。

# 用户指南

**烧录固件**

****步骤一: Windows 驱动安装****

(1) 打开 DriverAssitant 文件夹下的软件，该软件专为开发板驱动安装设计。

![2](https://github.com/shiviz-dev/rk3576/blob/adjustment_directory/Documents/images/2551f625c9584a9f228a7fabb5b53e94.jpg)

(2) 选择驱动安装选项，按照软件提示逐步操作，完成驱动安装，确保开发板与电脑能正常通信。

![3](https://github.com/shiviz-dev/rk3576/blob/adjustment_directory/Documents/images/6a3acd2996ee609f44f0e70e7a7b7a78.jpg)

****步骤二: 进入下载模式****

(1) 方法一：用电脑连接板端的 type - c 接口，长按 BOOT 按键，再开启电源，等待一两秒后松开 BOOT 按键，此时开发板成功进入下载模式。

![4](https://github.com/shiviz-dev/rk3576/blob/adjustment_directory/Documents/images/ca1f0a4fca70c4be22c16cbfc498c36c.jpg)

(2) 方法二：使用DEBUG或者ADB打开终端输入指令“reboot loader”进入下载模式

****步骤三: 烧录****

******Windows刷机******

(1) 在电脑端打开 RKDevTool 软件，若软件底部显示 “发现一个 LOADER 设备”，说明板子已进入下载模式，可进行后续烧录操作。

![5](https://github.com/shiviz-dev/rk3576/blob/adjustment_directory/Documents/images/665f35172233570bdf9825aefc33a39d.jpg)

(2) 在下载镜像界面，开发者可根据实际需求，选择单独烧录某一部分的镜像，灵活满足不同开发场景。

![6](https://github.com/shiviz-dev/rk3576/blob/adjustment_directory/Documents/images/36729c52203d8c3d6b336c118b982f41.jpg)

(3) 在升级固件界面，可选择烧录整个固件，一次性完成系统的更新或安装。

![7](https://github.com/shiviz-dev/rk3576/blob/adjustment_directory/Documents/images/f023aadacca7fe22cb682e0ddec993c6.jpg)

(4) 等待烧录完成，烧录过程中请保持开发板与电脑的连接稳定，避免因连接问题导致烧录失败。

![8](https://github.com/shiviz-dev/rk3576/blob/adjustment_directory/Documents/images/32df832a964e33e1f5cf0abacb02afc2.jpg)

******Linux刷机******

使用指令: 
```bash 
sudo./upgrade_tool uf update.img
```

其中 update.img 为要烧录的系统镜像


# 参数配置

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


# 资源下载

****文档链接****

[rk3576.doc](https://github.com/shiviz-dev/rk3576/blob/adjustment_directory/Documents/RK3576.doc)

[镜像文件下载](https://github.com/shiviz-dev/rk3576-dev-board/releases/)
