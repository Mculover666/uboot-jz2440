>本项目在Gitee的镜像地址：https://gitee.com/mculover666/uboot-jz2440

# 1. 已经适配的uboot版本

- uboot.2012.04.01

# 2. 编译方法

以 uboot-2012.04.01为例。

解压源码：
```bash
tar -jxf u-boot-2012.04.01.tar.bz2
```
进入源码文件夹：
```bash
cd u-boot-2012.04.01
```
打补丁：
```bash
patch -p1 < ../u-boot-2012.04.01-jz2440.patch
```
编译：
```bash
make distclean
make smdk2440_config
make
```
编译完成之后，在当前目录下生成u-boot.bin文件。

# 3. tftp_root文件夹

这个文件夹是JZ2440开发板官方提供的内核镜像文件和yaffs2文件系统镜像，用于测试uboot。

# 4. 移植教程/uboot研读笔记

- [00 - 嵌入式Linux系统中Bootloader的作用和基本运行原理](https://blog.csdn.net/Mculover666/article/details/104396179)
- [01 - 下载uboot源码并使用VSCode远程查看源码、编译uboot（2012.04.01版本）](https://blog.csdn.net/Mculover666/article/details/104398413)
- [02 - 详细探索uboot启动过程（基于S3C2410处理器）](https://blog.csdn.net/Mculover666/article/details/104401102)
- [03 - 初步移植uboot 2012.04到JZ2440（修改时钟，配置串口）](https://blog.csdn.net/Mculover666/article/details/104484787)
- [04 - 移植uboot 2012.04到JZ2440（支持Nor Flash读写）](https://blog.csdn.net/Mculover666/article/details/104501251)
- [05 - 移植uboot 2012.04到JZ2440（支持Nand Flash读写）](https://blog.csdn.net/Mculover666/article/details/104531452)
- [06 - 移植uboot 2012.04到JZ2440（支持DM9000C网卡）](https://blog.csdn.net/Mculover666/article/details/104549535)
- [07 - 移植uboot 2012.04到JZ2440（裁剪uboot大小）](https://blog.csdn.net/Mculover666/article/details/104564301)
- [08 - 移植uboot 2012.04到JZ2440（设置mtd分区表）](https://blog.csdn.net/Mculover666/article/details/104569790)
- [09 - 移植uboot 2012.04到JZ2440（设置默认环境变量参数）](https://blog.csdn.net/Mculover666/article/details/104558447)
- [10 - 移植uboot 2012.04到JZ2440（烧写Linux内核、烧写yaffs2文件系统）](https://blog.csdn.net/Mculover666/article/details/104586654)
- [11 - 移植uboot 2012.04到JZ2440（移植完成，制作uboot补丁）](https://blog.csdn.net/Mculover666/article/details/104588755)

# 5. 项目作者

Mculover666

- site： www.mculover666.cn
- blog:  mculover666.blog.csdn.net
- email: 2412828003@qq.com
