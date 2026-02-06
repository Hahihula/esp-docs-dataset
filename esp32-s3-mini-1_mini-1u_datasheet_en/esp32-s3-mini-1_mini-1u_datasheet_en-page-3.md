**1 Module Overview**

### 1.2 Series Comparison

ESP32-S3-MINI-1 and ESP32-S3-MINI-1U are two powerful, generic Wi-Fi + Bluetooth LE MCU modules that feature a rich set of peripherals, yet an optimized size. They are an ideal choice for a wide variety of application scenarios related to Internet of Things (IoT), such as embedded systems, smart home, wearable electronics, etc.

ESP32-S3-MINI-1 comes with a PCB antenna. ESP32-S3-MINI-1U comes with a connector for an external antenna. They feature an up to 8 MB SPI flash and an optional 2 MB SPI Pseudo static RAM (PSRAM). Both ESP32-S3-MINI-1 and ESP32-S3-MINI-1U come in two versions, with the ordering code ending with -N8 and -N4R2 respectively. The two versions only vary in flash and PSRAM size.

The series comparison for the two modules is as follows:

| Ordering Code | Flash^1, 2 | PSRAM | Ambient Temp ^3 (°C) | Size^4 (mm) |
|---------------|-----------|-------|----------------------|------------|
| ESP32-S3-MINI-1-N8 | 8 MB (Quad SPI) | - | - | 15.4 x 20.5 x 2.4 |
| ESP32-S3-MINI-1-N4R2 | 4 MB (Quad SPI) | 2 MB (Quad SPI) | -40 ~ 85 | -
| ESP32-S3-MINI-1-U-N8 | 8 MB (Quad SPI) | 2 MB (Quad SPI) | -40 ~ 85 | 15.4 x 15.4 x 2.4 |
| ESP32-S3-MINI-1-U-N4R2 | 4 MB (Quad SPI) | 2 MB (Quad SPI) | -40 ~ 85 | 15.4 x 15.4 x 2.4 |

1 For specifications, refer to Section [6.5 Memory Specifications](#).
2 By default, the SPI flash on the module operates at a maximum clock frequency of 80 MHz and does not support the auto suspend feature.
3 Ambient temperature specifies the recommended temperature range of the environment immediately outside the Espressif module.

At the core of the modules is an ESP32-S3 series SoC, an Xtensa® 32-bit LX7 CPU that operates at up to 240 MHz. You can power off the CPU and make use of the low-power co-processor to constantly monitor the peripherals for changes or crossing of thresholds.

**Note:**
For more information on ESP32-S3, please refer to [ESP32-S3 Series Datasheet](#).
For chip revision identification, ESP-IDF release that supports a specific chip revision, and other information on chip revisions, please refer to [ESP32-S3 Series SoC Errata > Section Chip Revision Identification](#).

### 1.3 Applications

- Smart Home
- Industrial Automation
- Health Care
- Consumer Electronics
- POS Machines
- Service Robot
- Audio Devices
- Generic Low-power IoT Sensor Hubs
- Smart Agriculture
- Generic Low-power IoT Data Loggers