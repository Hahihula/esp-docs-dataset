

# Chapter 54

## SD/MMC Host Controller (SDHOST)

### 54.1 Overview

The ESP32-P4 memory card interface controller provides a hardware interface between the Advanced Peripheral Bus (APB) and an external memory device. The memory card interface allows the ESP32-P4 to be connected to SDIO (secure digital I/O) memory cards, MMC (multimedia cards) and devices with a CE-ATA (Consumer Electronics Advanced Transport Architecture) interface. It supports two external cards (Card0 and Card1). All SD/MMC module interface signals only connect to GPIO pins via GPIO matrix.

### 54.2 Features

This module supports the following features:

* Two external cards
* SD memory Card specification V3.0 and V3.01, with a maximum transfer rate of DDR50
* MMC: V4.41, V4.5, and V4.51, with a maximum transfer rate of DDR50
* CE-ATA: V1.1
* 1-bit, 4-bit, and 8-bit modes

The SD/MMC controller topology is shown in Figure 54.2-1. The controller supports two peripherals, but they cannot function at the same time.

![Figure 54.2-1. SD/MMC Controller Topology](image-placeholder)

*Host Controller*

Data width 1/4/8 bits → Card0  
Data width 1/4 bits → Card1

SD Mem  
SDIO  
EMMC  
CE-ATA  

SD Mem  
SDIO  
EMMC  
CE-ATA