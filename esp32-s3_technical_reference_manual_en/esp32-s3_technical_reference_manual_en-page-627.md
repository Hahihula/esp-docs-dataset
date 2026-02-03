**Chapter Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Section Header:**
Register 10.56. RTC_CNTL_RTC_USB_CONF_REG (0x0120)

**Continuation Note:**
Continued from the previous page...

**Field Descriptions and Values with Details on Validity Conditions in Italicized Texts for Fields:**

- **RTC_CNTL_USB_PAD_ENABLE_OVERRIDE**: Set this bit to enable controlling the internal USB transceiver’s function via software. (R/W)
  
- **RTC_CNTL_USB_PAD_ENABLE**: Set this bit to enable the USB transceiver function. This field is valid when RTC_CNTL_USB_PAD_ENABLE_OVERRIDE is set. (R/W)

- **RTC_CNTL_USB_TXM**: Configures the USB D- tx value in test mode.
  - *This field is valid when RTC_CNTL_USB_TXM OVERRIDE is set.(R/W)*

- **RTC_CNTL_USB_TXP**: Configures the USB D+ tx value in test mode. 
  - *This field is valid when RTC_CNTL_USB_TXP OVERRIDE is set.(R/W)*

- **RTC_CNTL_USB_TX_EN**: Configures the USB pad open in test mode.
  - *This field is valid when RTC_CNTL_USB_TX_EN OVERRIDE is set. (R/W)*

- **RTC_CNTL_USB_TX_EN_OVERRIDE**: Set this bit to enable controlling the internal USB transceiver Tx in test mode via software.

- **RTC_CNTL_USB_RESET_DISABLE**: Set this bit to disable reset USB OTG.
  - *This field is valid when RTC_CNTL_USB_RESET_DISABLE is set. (R/W)*

- **RTC_CNTL_IO_MUX_RESIST_DISABLE**: Set this bit to disable reset IO MUX and GPIO Matrix.
  - *This field is valid when RTC_CNTL_IO_MUX_RESIST OVERRIDE is set.(R/W)*

- **RTC_CNTL_SW_USB_PHY_SEL**: Set this bit to allow USB OTG to use the internal USB transceiver. Clear this bit to allow USB-Serial-JTAG to use the internal USB transceiver.
  - *This field is valid when RTC_CNTL_SW_HW_USB_PHY_SEL is set. (R/W)*

- **RTC_CNTL_SW_HW_USB_PHY_SEL**: Set this bit to control the internal USB transceiver selection via software
  - *RTC_CNTLangle SW_USB_PHY_SEL). Clear this bit to control the the internal USB transceiver selection via hardware (eFuse).
  - This field is valid when RTC_CNTLangle SW_USB_PHY OVERRIDE is set. (R/W)*

**Field Description:**
- **RTC_CNTL_REJECT_CAUSE**: Stores the reject-to-sleep cause.
  - *Stores the reject-to-sleep cause.* (RO)

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback