**Chapter Title:**
Chapter 28 I2S Controller (I2S)

**Section Header:**
Register 28.15. I2S_TX_TDM_CTRL_REG (0x0054)

**Continuation Note:**
Continued from the previous page...

**Body Text with List Items and Descriptions for Each Item in Register:**

- **I2S_TX_TDM_CHAN10_EN**: 1 - Enable the valid data output of I2S TX TDM channel 10. O: Channel TX data is controlled by `I2S_TX_CHAN_EQUAL` and `I2S_SINGLE_DATA`. See Section [28.9.2.1](#). (R/W)
  
- **I2S_TX_TDM_CHAN11_EN**: 1 - Enable the valid data output of I2S TX TDM channel 11. O: Channel TX data is controlled by `I2S_TX_CHAN_EQUAL` and `I2S_SINGLE_DATA`. See Section [28.9.2.1](#). (R/W)
  
- **I2S_TX_TDM_CHAN12_EN**: 1 - Enable the valid data output of I2S TX TDM channel 12. O: Channel TX data is controlled by `I2S_TX_CHAN_EQUAL` and `I2S_SINGLE_DATA`. See Section [28.9.2.1](#). (R/W)
  
- **I2S_TX_TDM_CHAN13_EN**: 1 - Enable the valid data output of I2S TX TDM channel 13. O: Channel TX data is controlled by `I2S_TX_CHAN_EQUAL` and `I2S_SINGLE_DATA`. See Section [28.9.2.1](#). (R/W)
  
- **I2S_TX_TDM_CHAN14_EN**: 1 - Enable the valid data output of I2S TX TDM channel 14. O: Channel TX data is controlled by `I2S_TX_CHAN_EQUAL` and `I2S_SINGLE_DATA`. See Section [28.9.2.1](#). (R/W)
  
- **I2S_TX_TDM_CHAN15_EN**: 1 - Enable the valid data output of I2S TX TDM channel 15. O: Channel TX data is controlled by `I2S_TX_CHAN_EQUAL` and `I2S_SINGLE_DATA`. See Section [28.9.2.1](#). (R/W)
  
- **I2S_TX_TDM_TOT_CHAN_NUM**: Set the total number of channels in use in I2S TX TDM mode. Total channel number in use = this value + 1. (R/W)

- **I2S_TX SKIP_MSK_EN**: When DMA TX buffer stores data of (`I2S_TX_TDMTot_CHAN_NUM + 1`) channels, and only the data of the enabled channels is sent, then this bit should be set. Clear it when all the data stored in DMA TX buffer is for enabled channels.

**Footer:**
Espressif Systems
Page Number: 1072

**Document Information:**
ESP32-S3 TRM (Version 1.7)

**Navigation Links:**
GoBack, Submit Documentation Feedback