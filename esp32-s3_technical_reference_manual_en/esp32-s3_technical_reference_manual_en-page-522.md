**Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**Header:**
Register 6.53. RTC_IO_XTAL_32P_PAD_REG (0x0C0)

**Diagram/Block Diagram Description:**
A block diagram showing various registers with labels such as "RTC_IO_X32P_DRV", "RTC_IO_X32P_RDE", etc., and their corresponding bit positions.

**Table/List of Registers:**

- **RTC_IO_X32PFUN_IE**: Input enable in normal execution. (R/W)
- **RTC_IO_X32PSLP_OE**: Output enable in sleep mode. (R/W)
- **RTC_IO_X32PSLPIE**: Input enable in sleep mode. (R/W)
- **RTC_IO_X32PSLPSEL**: 1: enable sleep mode; 0: no sleep mode. (R/W)
- **RTC_IO_X32PFUN_SEL**: Function selection. (R/W)
- **RTC_IO_X32PMUX SEL**: 1: use RTC GPIO; 0: use digital GPIO. (R/W)
- **RTC_IO_X32PRUE**: Pull-up enable of the pin. 1: internal pull-up enabled; 0: internal pull-up disabled. (R/W)
- **RTC_IO_X32P RDE**: Pull-down enable of the pin. 1: internal pull-down enabled, 0: internal pull-down disabled. (R/W)
- **RTC_IO_X32P_DRV**: Select the drive strength of the pin. 0: ~5 mA; 1: ~10 mA; 2: ~20 mA; 3: ~40 mA. (R/W)

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Page Number and Document Version:**
ESP32-S3 TRM (Version 1.7)