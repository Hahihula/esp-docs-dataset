**Chapter Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**Section Header:**
Register 6.53. RTCIO_TOUCH_PADn_REG (n: 0-7) (0x94+4*n)

**Table Description:**
The table lists various registers related to touch pad control on the ESP32.

| Register Name | Offset |
|---------------|--------|
| RTCIO_TOUCH_PADn_HOLD | 0 |
| RTCIO TOUCH PADn_DRV | 1 |
| ... | ... |

**Text Content with Descriptions of Registers and Their Functions:**

- **RTCIO_TOUCH_PADn_HOLD**
  - Description: Write 1 to hold the current value of the output. (R/W)

- **RTCIO_TOUCH_PADn_DRV**
  - Description: Selects the drive strength of the pin. A higher value corresponds with a higher strength.
  - Reference Note: For detailed drive strength, please see ESP32 Datasheet > Appendix A.1 Notes on ESP32 Pin Lists > Note 8.

- **RTCIO_TOUCH_PADn_RDE**
  - Description: Pull-down on pin enabled; 0: Pull-down disabled (R/W)

- **RTCIO TOUCH PADn RUE**
  - Description: Pull-up on pin enabled; 0: Pull-up disabled. (R/W)

- **RTCIO_TOUCH_PADn_DAC**
  - Description: Touch sensor slope control.
  - Details: 3-bit for each touch pin, default is b'100.

- **RTCIO TOUCH PADn START**
  - Description: Write 1 to start the touch sensor. (R/W)

- **RTCIO_TOUCH_PADn_TIE_OPT**
  - Description: Default touch sensor tie option.
  - Values:
    - `0`: Tied to VDD_RTC voltage
    - `1`: Reserved

- **RTCIO TOUCH PADn_XPD**
  - Description: Write 1 to power on the touch sensor. (R/W)

- **RTCIO_TOUCH_PADn_MUX_SEL**
  - Description: Selects RTC IO_MUX or IO_MUX to control the IE/OE/RUE/RDE statues of RTC pin.
  - Values:
    - `1`: Selects RTC IO_MUX
    - `0`: Selects IO_MUX

- **RTCIO TOUCH PADn_FUNC_SEL**
  - Description: Selects the function of the RTC.
  - Values:
    - `0`: RTC Function O
    - `1`: Reserved
    - `2`: Reserved
    - `3`: RTC Function 1 (R/W)

- **RTCIO_TOUCH_PADn_SLP_SEL**
  - Description: Sleep mode selection signal of the pin. Set this bit to 1 to put the pin to sleep.
  - Values:
    - `(R/W)`

**Footer Note:** Continued on the next page...

**Company Information and Document Version:**
Espressif Systems
ESP32 TRM (Version 5.6)

**Navigation Links:**
- Submit Documentation Feedback

(Note: The table in the image is not fully transcribed due to its complexity, but it provides a structured overview of various touch pad control registers.)