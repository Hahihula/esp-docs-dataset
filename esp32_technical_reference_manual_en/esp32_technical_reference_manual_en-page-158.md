**Chapter Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**Register Information:**
- **Register Name:** RTCIO_PAD_DAC2_REG (0x0088)
- **Bit Description Table:**

| Bit | Description |
|-----|-------------|
| 31  | Reserved   |
| 30  | RTCIO_PAD_PDAC2_DRV |
| 29  | RTCIO_PAD_PDAC2_HOLD |
| 28  | RTCIO_PAD_PDAC2_RDE |
| 27  | RTCIO_PAD_PDAC2_RUE |
| 26  | Reserved   |
| ... | ...         |
| 0   | RTCIO_PAD_DAC2_FORCE |

**Field Descriptions:**

- **RTCIO_PAD_PDAC2_DRV:** Select the drive strength of the pin. (R/W)
- **RTCIO_PAD_PDAC2_HOLD:** Set to 1 to hold the output value on the pin; O is for normal operation.
  - (R/W)
- **RTCIO_PAD_PDAC2_RDE:** Pull-down on pin enabled; 0: Pull-down disabled. (R/W)
- **RTCIO_PAD_PDAC2_RUE:** Pull-up on pin enabled; 0: Pull-up disabled. (R/W)
- **RTCIO_PAD_PDAC2_DAC:** Pin DAC2 output value.
  - (R/W)
- **RTCIO_PAD_PDAC2_XPD_DAC:** Power on DAC2. PDAC2 needs to be tristated if we power on the DAC, i.e., IE=0, OE=0, RDE=0, RUE=0. (R/W)
- **RTCIO_PAD_PDAC2_MUX_SEL:** route pin to the digital IO_MUX; (R/W)
  - Route selection: 
    - 1: route to the RTC block
- **RTCIO_PAD_PDAC2_FUN_SEL:** Select the RTC function for this pin.
  - Set select Function O. (R/W)
- **RTCIO_PAD_PDAC2_SLP_SEL:** Sleep mode selection signal of the pin.
  - Set this bit to 1 to put the pin to sleep: 
    - (R/W)
- **RTCIO_PAD_PDAC2_SLP_IEN:** Input enable of the pin in sleep mode.  
  - 1: enabled; O: disabled. (R/W)
- **RTCIO_PAD_PDAC2_SLP_OEN:** Output enable of the pin.
  - 1: enabled; O: disabled. (R/W)
- **RTCIO_PAD_PDAC2FUNIE:** Input enable of the pin:
  - 1: enabled; O: disabled. (R/W)
- **RTCIO_PAD_DAC2_DAC_XPD_FORCE:** Power on DAC2.
  - Usually, we need to tristate PDAC2 if we power on the DAC,
    - i.e., IE=0, OE=0, RDE=0, RUE=0. (R/W)

**Footer:**
- Page number: 158
- Document version: ESP32 TRM (Version 5.6)
- Company name: Espressif Systems

**Navigation Links:** 
- Submit Documentation Feedback