# 适用于Nanopc-t1的uboot

## 简介

## 编译

```
cd uboot-nanopc-t1
make tiny4412_config
make
```
## 烧写uboot镜像到SD卡

### 准备必要工具

```
cd sd_fuse
make
```

### 烧写uboot到SD卡

```
cd tiny4412
sudo ./sd_fusing.sh YOUR_SD_DEVICE #such as /dev/sdb
```
## 上机测试

1. 插上SD卡，选择从SD卡启动

下面是启动时的终端输出:

```
OK

U-Boot 2010.12-00000-g8ac4182-dirty (Mar 01 2015 - 11:56:19) for TINY4412


CPU:    S5PC220 [Samsung SOC on SMP Platform Base on ARM CortexA9]
        APLL = 1500MHz, MPLL = 800MHz

Board:  TINY4412
DRAM:   2047 MiB

vdd_arm: 1.2
vdd_int: 1.0
vdd_mif: 1.1

BL1 version:  N/A (TrustZone Enabled BSP)


Checking Boot Mode ... SDMMC
REVISION: 1.1
MMC Device 0: 15193 MB
MMC Device 1: 7456 MB
MMC Device 2: N/A
*** Warning - using default environment                                         
                                                                                
Net:    No ethernet found.                                                      
Hit any key to stop autoboot:  0
TINY4412 #
```

## 特别感谢

1. wanyuhang提供的补丁: <http://www.arm9home.net/read.php?tid-83336-uid-105026.html>