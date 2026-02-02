**Chapter Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**Section Header:**
GoBack

**Register Information Section:**

- **Title:** Register 6.54. RTCIO_TOUCH_PADm_REG (m = 8, 9) (0x0B4, 0x00B8)
  
  - **Field Descriptions and Values for m=8:**
    - `RTCIO_TOUCH_PADm_DAC`: Touch sensor slope control. 3-bit for each touch pin. Default b'100.
      - **Register Access:** (R/W)
    - `RTCIO TOUCH_PADm START`: Write 1 to start touch sensor. (R/W)
    - `RTCIO_TOUCH_PADm TIE_OPT`: Default touch sensor tie option
      - Values:
        - `0`: Tied to O V
        - `1`: Tied to VDD_RTC voltage

  - **Field Descriptions and Values for m=9:**
    - `RTCIO TOUCH_PADm_XPD`: Write 1 to power on the touch sensor. (R/W)
    - `RTCIO_TOUCH_PADm_TO_GPIO`: Controls the routing of touch pin input signals to IO_MUX.
      - Values:
        - `0`: The input signal from the touch pin is routed through analog function
        - `1`: The input signal from the touch pin is routed via IO_MUX

- **Title:** Register 6.55. RTCIO_EXT_WAKEUPO_REG (0x00BC)

  - **Field Description:**
    - `RTCIO_EXT_WAKEUPO_SEL`: GPIO[0-17] can be used to wake up the chip when the chip is in sleep mode.
      - This register prompts the pin source to wake up the chip when it's either deep or light sleep mode. 
      - Values:
        - `0`: select GPIO0
        - `1`: select GPIO2, etc.

**Footer:**
Espressif Systems  
Submit Documentation Feedback

**Page Number and Document Version:** 163 ESP32 TRM (Version 5.6)