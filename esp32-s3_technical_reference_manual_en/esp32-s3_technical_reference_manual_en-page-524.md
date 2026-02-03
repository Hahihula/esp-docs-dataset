**Title: Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)**

---

### Register Description:
- **Register Name:** RTC_IO_RTC_PADn_REG  
- **Address Range:** n : 17-21  
- **Addresses in Hexadecimal:** 0x0C08, 0x0CC0, 0x0D00, 0x0D4, 0x0D8

---

### Bit Description:
| Address | Name | Description |
|---------|------|-------------|
| 31      | (reserved) | Reserved bit. |
| ...     | ...   | ...         |

#### Specific Bits and Their Functions:

- **Bit 29:** RTC_IO_RTC_PADn_DRV  
  - Input enable in normal execution: R/W

- **Bit 28:** RTC_IO_RTC_PADn_RDE  
  - Output enable in sleep mode: R/W

- **Bit 27:** RTC_IO_RTC_PADn_SLP_CDE  
  - Output enable in sleep mode. (R/W)

- **Bit 26:** RTC_IO_RTC_PADn_SLP_IDE  
  - Input enable in sleep mode. (R/W)

- **Bit 25:** RTC_IO_RTC_PADn_SLP_SEL  
  - Enable sleep mode: O; no sleep mode. (R/W)
    - Value `0`: No Sleep Mode
    - Value `1`: Enable Sleep Mode

- **Bit 24:** RTC_IO_RTC_PADn_FUN_SEL  
  - Function selection:
    - Use RTC GPIO.
    - Use digital GPIO.

- **Bit 23:** RTC_IO_RTC_PADn_MUXSEL  
  - Pull-up enable of the pin: 
    - Internal pull-up enabled (Value `1`).
    - Internal pull-up disabled (Value `0`).

- **Bit 22:** RTC_IO_RTC_PADn_RDE  
  - Pull-down enable of the pin:
    - Internal pull-down enabled.
    - Internal pull-down disabled.

---

### Drive Strength Selection:

- **RTC_IO_RTC_PADn_DRV**
  - Selects drive strength for the pin based on the following values (R/W):
    - `0`: ~5 mA
    - `1`: ~20 mA
    - `2`: ~10 mA
    - `3`: ~40 mA

- **Other RTC GPIOs:**
  - Selects drive strength for other RTC GPIO pins based on the following values (R/W):
    - `0`: ~5 mA
    - `1`: ~10 mA
    - `2`: ~20 mA
    - `3`: ~40 mA

---

**Footer Information:**
- **Company:** Espressif Systems
- **Document Version:** ESP32-S3 TRM (Version 1.7)
- **Page Number:** 524