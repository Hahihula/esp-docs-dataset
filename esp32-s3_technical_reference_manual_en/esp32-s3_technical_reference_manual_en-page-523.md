**Title: Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)**

**Subtitle: Register 6.54. RTC_IO_XTAL_32N_PAD_REG (0x0C4)**

**Table Description:**
- The table lists various registers with their corresponding bit positions.
- Columns include:
  - Bit position numbers ranging from 'reserved' to specific register names like `RTC_IO_X32N_DRV`, `RTC_IO_X32N_RDE`, etc.

**Text Descriptions for Registers and Functions:**

1. **RTC_IO_X32N_FUN_IE**
   - Description: Input enable in normal execution.
   - Access Rights (R/W): Read/Write

2. **RTC_IO_X32N_SLP_OE**
   - Description: Output enable in sleep mode.
   - Access Rights (R/W): Read/Write

3. **RTC_IO_X32N_SLP_IE**
   - Description: Enable input enable in sleep mode.
   - Access Rights (R/W): Read/Write

4. **RTC_IO_X32N_SLP_SEL**
   - Description: 1: enable sleep mode; 0: no sleep mode.
   - Access Rights (R/W): Read/Write

5. **RTC_IO_X32N_FUN_SEL**
   - Description: Function selection.

6. **RTC_IO_X32N_MUX_SEL**
   - Description: 1: use RTC GPIO; 0: use digital GPIO.
   - Access Rights (R/W): Read/Write

7. **RTC_IO_X32N_RUE**
   - Description: Pull-up enable of the pin:
     - 1: internal pull-up enabled
     - 0: internal pull-up disabled.

8. **RTC_IO_X32N_RDE**
   - Description: Pull-down enable of the pin.
     - 1: internal pull-down enabled, 
     - 0: internal pull-down disabled (R/W)

9. **RTC_IO_X32N_DRV**
   - Description: Select the drive strength of the pin:
     - 0: ~5 mA
     - 1: ~10 mA
     - 2: ~20 mA
     - 3: ~40 mA (R/W)

**Footer Information:**

- **Company:** Espressif Systems
- **Document Version:** ESP32-S3 TRM (Version 1.7)
- **Page Number:** 523

**Link Texts:**
- Submit Documentation Feedback