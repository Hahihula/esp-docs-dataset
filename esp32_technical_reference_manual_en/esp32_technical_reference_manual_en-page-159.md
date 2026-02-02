**Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**Header:**
Register 6.51. RTCIO_XTAL_32K_PAD_REG (0x08C)

**Table:**
- The table lists various registers related to the XTAL_32K module with their respective bit positions.
- Bits are labeled from '31' down to '0'.
- Each register is associated with a specific function or setting, such as drive strength selection ('DRV'), hold settings for different pins.

**Body Text:**
- **RTCIO_XTAL_X32N_DRV**: Select the drive strength of the pin. (R/W)
  - Set to `1` to hold the output value on the pin; `0` is for normal operation.
  
- **RTCIO_XTAL_X32N_HOLD**:
  - R/W
  
- **RTCIO_XTAL_X32N_RDE**: Pull-down on pin enabled: `1`; Pull-down disabled: `0`. (R/W)
  
- **RTCIO_XTAL_X32N_RUE**: Pull-up on pin enabled: `1`; Pull-up disabled: `0`. (R/W)
  
- **RTCIO_XTAL_X32P_DRV**: Select the drive strength of the pin. (R/W)
  
- **RTCIO_XTAL_X32P_HOLD**:
  - Set to `1` to hold the output value on the pin, `0` is for normal operation.
  
- **RTCIO_XTAL_X32P_RDE**: Pull-down on pin enabled: `1`; Pull-down disabled: `0`. (R/W)
  
- **RTCIO_XTAL_X32P_RUE**: Pull-up on pin enabled: `1`; Pull-up disabled: `0`. (R/W)
  
- **RTCIO_XTAL_DAC_XTAL_32K**: 32K XTAL bias current DAC value. (R/W)
  
- **RTCIO_XTAL_XPD_XTAL_32K**: Power up 32 KHz crystal oscillator. (R/W)
  
- **RTCIO_XTAL_X32N_MUX_SEL**:
  - `0`: route X32N pin to the digital IO_MUX; `1`: route to RTC block.
  
- **RTCIO_XTAL_X32P_MUX_SEL**:
  - `0`: route X32P pin to the digital IO_MUX; `1`: route to RTC block.
  
- **RTCIO_XTAL_X32N_FUN_0**: Select the RTC function. `0`: select function `0`. (R/W)
  
- **RTCIO_XTAL_X32N_SLP_SEL**:
  - Sleep mode selection: Set this bit `1` to put the pin in sleep.
  
- **RTCIO_XTAL_X32N_SLPIBE**: Input enable of the pin in sleep mode. `1`: enabled; `0`: disabled. (R/W)
  
- **RTCIO_XTAL_X32N_SLPOE**: Output enable of the pin. `1`: enabled; `0`: disabled. (R/W)
  
- **RTCIO_XTAL_X32NFUNIBE**: Input enable of the pin in sleep mode.
  - `1`: enabled; `0`: disabled.

**Continued on next page...**

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32 TRM (Version 5.6)