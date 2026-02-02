**Chapter Title:**
Chapter 22 I2S Controller (I2S)

**Section Header:**
Register 22.12. I2S_CONF_CHAN_REG (0x002c)

**Body Text and Table Description for I2S_CONF_CHAN_REG:**

- **Field Name:** `I2S_RX_CHAN_MOD`
  - **Description:** I2S receiver channel mode configuration bits.
  - **Reference:** Please refer to Section 22.4.5
  - **Access Mode:** (R/W)

- **Field Name:** `I2S_TX_CHAN_MOD`
  - **Description:** I2S transmitter channel mode configuration bits.
  - **Reference:** Please refer to Section 22.4.4
  - **Access Mode:** (R/W)

**Section Header:**
Register 22.13. I2S_OUT_LINK_REG (0x0030)

**Body Text and Table Description for I2S_OUT_LINK_REG:**

- **Field Name:** `I2S_OUTLINK_RESTART`
  - **Description:** Set this bit to restart outlink descriptor.
  - **Access Mode:** (R/W)
  
- **Field Name:** `I2S_OUTLINK_START`
  - **Description:** Set this bit to start outlink descriptor.
  - **Access Mode:** (R/W)

- **Field Name:** `I2S_OUTLINK_STOP`
  - **Description:** Set this bit to stop outlink descriptor.
  - **Access Mode:** (R/W)
  
- **Field Name:** `I2S_OUTLINK_ADDR`
  - **Description:** The address of first outlink descriptor.
  - **Access Mode:** (R/W)

**Section Header:**
Register 22.14. I2S_IN_LINK_REG (0x0034)

**Body Text and Table Description for I2S_IN_LINK_REG:**

- **Field Name:** `I2S_INLINK_RESTART`
  - **Description:** Set this bit to restart inlink descriptor.
  - **Access Mode:** (R/W)
  
- **Field Name:** `I2S_INLINK_START`
  - **Description:** Set this bit to start inlink descriptor.
  - **Access Mode:** (R/W)

- **Field Name:** `I2S_INLINK_STOP`
  - **Description:** Set this bit to stop inlink descriptor.
  - **Access Mode:** (R/W)
  
- **Field Name:** `I2S_INLINK_ADDR`
  - **Description:** The address of first inlink descriptor.
  - **Access Mode:** (R/W)

**Footer:**
Espressif Systems
440 ESP32 TRM (Version 5.6) 
Submit Documentation Feedback