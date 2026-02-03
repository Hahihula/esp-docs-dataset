**Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Back Link:**
GoBack

**Register Information:**
- Register Name: RTC_CNTL_RTC_USB_CONF_REG (0x0120)
- Bit Positions and Descriptions:
  - **Bit 31:** Reserved.
  - **Bits 24 to 8:** Various control settings for USB-related functions such as SW_PHY_SEL, RESET_DISABLE, TX_EN, PULLDOWN, DM_PULLDOWN, VREF, etc.

**Field Descriptions:**
- **RTC_CNTL_USB_VREFH**: Controls the internal USB transceiver single-end input high threshold (1.76 V to 2 V, step 80 mV). This field is valid when RTC_CNTL_USB_VREF_OVERRIDE is set.
- **RTC_CNTL_USB_VREFL**: Controls the internal USB transceiver single-end input low threshold (0.8 V to 1.04 V, step 80 mV). This field is valid when RTC_CNTL_USB_VREF_OVERRIDE is set.
- **RTC_CNTL_USB_VREF OVERRIDE**: Set this bit to enable controlling the internal USB transceiver’s input voltage threshold via software.

**Additional Fields:**
- **RTC_CNTL_USB_PAD_PULL_OVERRIDE**, **RTC_CNTL_USB_DP_PULLUP**, etc.: Various settings for enabling or disabling pull-up and pull-down resistors on different pins, valid under specific conditions as described in each field.
  - For example:
    - **RTC_CNTL_USB_DM_PULUP**: Set this bit to enable USB- pull-up resistor. This field is valid when RTC_CNTL_USB_PAD_PULL_OVERRIDE is set.

**Continuation Note:**
Continued on the next page...

**Footer Information:**
- Company Name: Espressif Systems
- Document Version and Type: ESP32-S3 TRM (Version 1.7)
- Page Number: 626

**Action Links:**
- Submit Documentation Feedback