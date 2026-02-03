**Title: Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)**

**Register Information:**  
Register `6.52. RTC_IO_TOUCH_PADn_REG` (`n`: 0-14) `(0x084+0x4*n)`  

| Bit | Description |
|-----|-------------|
| 31:30 | Reserved |
| 29:27 | RTC_IO TOUCH_PADn_RDE |
| 26:25 | RTC_IO TOUCH_PADn_RUE |
| ... | ... |
| 0    | Reset |

**Field Descriptions:**  
- **RTC_IO_TOUCH_PADnFUNIE**: Input enable in normal execution. (R/W)
- **RTC_IO_TOUCH_PADnSLP_OE**: Output enable in sleep mode. (R/W)
- **RTC_IO TOUCH_PADnSLP_IE**: Input enable in sleep mode. (R/W)
- **RTC_IO_TOUCH_PADnSLP_SIE**: 0: no sleep mode; 1: enable sleep mode. (R/W)
- **RTC_IO_TOUCH_PADnFUNSEL**: Function selection. (R/W)
- **RTC_IO TOUCH_PADnMUXSEL**: Connect the RTC pin input or digital pin input. `0` is available, i.e., select digital pin input. (R/W)
- **RTC_IO_TOUCH_PADnXPDE**: Touch sensor power on. (R/W)
- **RTC_IO_TOUCH_PADnTIE_OPT**: The tie option of touch sensor: 0: tie low; 1: tie high. (R/W)
- **RTC_IO TOUCH_PADn斯塔**: Start touch sensor. (R/W)
- **RTC_IO_TOUCH_PADnRUNE**: Pull-up enable of the pin. `1`: internal pull-up enabled; `0`: internal pull-up disabled. (R/W)
- **RTC_IO_TOUCH_PADnRDPE**: Pull-down enable of the pin. `1`: internal pull-down enabled, `0`: internal pull-down disabled. (R/W)
- **RTC_IO TOUCH_PADnDRV**: Select the drive strength of the pin: 0: ~5 mA; 1: ~10 mA; 2: ~20 mA; 3: ~40 mA. (R/W)

**Footer:**  
Espressif Systems  
ESP32-S3 TRM (Version 1.7)  

[Submit Documentation Feedback](#)