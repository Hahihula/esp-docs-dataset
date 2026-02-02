**Title: Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)**

---

### Register Description:
- **Name:** RTCIO_PAD_DAC1_REG (0x0084)
- **Description:** This register is used to configure the DAC1 pin.

#### Bit Fields:

| Bit Field | Offset | Access Mode | Description |
|-----------|--------|-------------|------------|
| 31       | 31     | (R/W)       | Reset      |
| ...       | ...    | -           | -          |

- **RTCIO_PAD_PDAC1_DRV:** Select the drive strength of the pin. (R/W)
- **RTCIO_PAD_PDAC1_HOLD:** Set to 1 to hold the output value on the pin; set to 0 for normal operation.
- **RTCIO_PAD_PDAC1_RDE:** 
  - Pull-down on pin enabled: O
  - Pull-down disabled: R/W

- **RTCIO_PAD_PDAC1_RUE:** 
  - Pull-up on pin enabled: I
  - Pull-up disabled: (R/W)

- **RTCIO_PAD_PDAC1_DAC:** Pin DAC1 output value. (R/W)
- **RTCIO_PAD_PDAC1_XPD_DAC:** Power on DAC1. Usually, PDAC1 needs to be tristated if we power on the DAC, i.e., IE=0, OE=0, RDE=0, RUE=0.
- **RTCIO_PAD_PDAC1_MUX_SEL:** 
  - Route pin to the digital IO_MUX; (R/W)
  - 1: route to the RTC block
  - The functional selection signal of the pin. (R/W)

- **RTCIO_PAD_PDAC1_FUN_SLE:** Sleep mode selection signal of the pin. Set this bit to 1 to put the pin to sleep.
- **RTCIO_PAD_PDAC1_SLP_IEN:** Input enable of the pin in sleep mode; 
  - enabled: R/W
  - disabled: O

- **RTCIO_PAD_PDAC1_SLP_OEN:** Output enable of the pin. (R/W)
- **RTCIO_PAD_PDAC1FUN_IEN:** Input enable of the pin.
  - enabled it: I
  - disabled: (R/W)

- **RTCIO_PAD_PDAC1_DAC_XPD_FORCE:** Power on DAC1. Usually, we need to tristate PDAC1 if we power on the DAC; i.e., IE=0, OE=0, RDE=0, RUE=0.

---

**Footer:**
- Page number: 157
- Document version: ESP32 TRM (Version 5.6)
- Company name: Espressif Systems

[Submit Documentation Feedback](#)