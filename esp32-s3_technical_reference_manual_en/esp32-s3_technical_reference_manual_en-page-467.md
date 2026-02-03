**Chapter Title:**
Chapter 5 eFuse Controller

**Section Header:**
Register 5.105. EFUSE_CMD_REG (0x01D4)

**Table Description for Register 5.105, EFUSE_CMD_REG (0x01D4):**

- **Field Name:** EFUSE_BLK_NUM
  - **Description:** Configures whether or not to send read command.
    - **Values:**
      - `Send`: 1; No effect (`R/WS/SC`)
      - `No effect`: 0 (`R/WS/SC`)

- **Field Name:** EFUSE_PGM_CMD
  - **Description:** Configures whether or not to send programming command.
    - **Values:**
      - `Send`: 1; No effect (`R/WS/SC`)
      - `No effect`: 0 (`R/WS/SC`)

- **Field Name:** EFUSE_BLK_NUM
  - **Description:** Configures the index of the block to be programmed.
    - **Values:**
      - Value ranges from 0 to 10 correspondingly (`P/W`)
      - `Value 0 ~ 10 corresponds to block number 0 ~ 10 respectively.`

**Section Header:**
Register 5.106. EFUSE_DAC_CONF_REG (0x01E8)

**Table Description for Register 5.106, EFUSE_DAC_CONF_REG (0x01E8):**

- **Field Name:** EFUSE_OE_CLR
  - **Description:** Configures whether or not to reduce the power supply of the programming voltage.
    - **Values:**
      - `Reduce`: 1; No effect (`R/W`)
      - `No effect`: 0 (`R/W`)

**Section Header:**
Register 5.107. EFUSE_RD_TIM_CONF_REG (0x01EC)

**Table Description for Register 5.107, EFUSE_RD_TIM_CONF_REG (0x01EC):**

- **Field Name:** EFUSE_READ_INIT_NUM
  - **Description:** Configures the initial read time of eFuse.
    - **Values:**
      - `R/W`

**Footer Information:**
Espressif Systems  
467 ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback