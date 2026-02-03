**Related Documentation and Resources**

## Revision History

### Release Notes (2025-06-09, v1.7)

Updated the following chapters:

- **Chapter 4 System and MEMORY**: Added RMT information in Figure 4.3-2.
- **Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)**: Updated Figure 6.3-1 of Hold feature.

### Release Notes (2024-12-10, v1.6)

Updated the following chapters:

- **Chapter 8 Chip Boot Control**: Updated the latching condition for strapping pins.
- **Chapter 29 LCD and Camera Controller (LCD_CAM)**: Updated descriptions of register fields `LCD_CAM_LCD_HB_FRONT`, `LCD_CAM_LCD_VB_FRONT`, `LCD_CAM_LCD_HSYNC_POSITION`, and `LCD_CAM_LCD_HSYNC_WIDTH`.
- **Chapter 39 On-Chip Sensors and Analog Signal Processing**: Corrected "-0.5" to "+0.5" in the ADC filter formula.

Updated descriptions of predefined power modes:
- Added a note about EXT1 under Table 10.4-3.
- Marked TOUCH Active In table as a wake-up source in Deep-sleep mode for `LEDC_DUTY_START_CHn bit`.

### Additional Updates (2024-12-10, v1.6)

Updated the following chapters:

- **Chapter 10 Low-power Management (RTC_CNTL)**:
  - Updated descriptions of predefined power modes.
  
- **Chapter 35 LED PWM Controller (LEDC)**: Updated description for `LEDC_DUTY_START_CHn bit`.

- **Chapter 39 On-Chip Sensors and Analog Signal Processing**:
  - Removed descriptions about the internal voltage/signal in SAR ADC2 measurement.
  - Added notes on touch sensor wake-up source when RTC Peripherals power domain is off, as well as when TOUCH Timeout is enabled for a wake-up source.

Updated measurements of temperature sensors:

- Updated range information from Table 39.4-1 Temperature Measurement Range and Offset (Cont'd on next page).

---

**Espressif Systems**

**Submit Documentation Feedback**

ESP32-S3 TRM (Version 1.7)