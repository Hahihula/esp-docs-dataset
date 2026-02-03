**Title: Chapter 30 SPI Controller (SPI)**

**Register Information:**  
- **Name:** SPI_DIN_NUM_REG  
- **Address:** 0x0028  

**Binary Representation Diagram of Register:**
```
+-----+-----+-----+-----+-----+-----+-----+-----+
|     |     |     |     |     |     |     |     |
+-----+-----+-----+-----+-----+-----+-----+-----+
| 31  | 30  | 29  | 28  | 27  | 26  | 25  | 24  |
+-----+-----+-----+-----+-----+-----+-----+-----+
|     |     |     |     |     |     |     |     |
+-----+-----+-----+-----+-----+-----+-----+-----+
| SPI_DIN7_NUM (for SPI2 only) | Configure the delays to input data bit7 signal based on the setting of SPI_DIN7_MODE. Can be configured in CONF state. (R/W)
+-----+-----+-----+-----+-----+-----+-----+-----+
```

**Description:**
- **SPI_DINO_NUM:** Configure the delays to input data bit0 signal based on the setting of SPI_DINO_MODE.
  - Can be configured in CONF state.

- **SPI_DIN1_NUM:** Configure the delays to input data bit1 signal based on the setting of SPI_DIN1_MODE. 
  - Can be configured in CONF state (R/W).

- **SPI_DIN2_NUM:** Configure the delays to input data bit2 signal based on the setting of SPI_DIN2_MODE.
  - Can be configured in CONF state.

- **SPI_DIN3_NUM:** Configure the delays to input data bit3 signal based on the setting of SPI_DIN3_MODE. 
  - Can be configured in CONF state (R/W).

- **SPI_DIN4_NUM (for SPI2 only):** Configure the delays to input data bit4 signal based on the setting of SPI_DIN4_MODE.
  - Can be configured in CONF state.

- **SPI_DIN5_NUM (for SPI2 only):** Configure the delays to input data bit5 signal based on the setting of SPI_DIN5_MODE. 
  - Can be configured in CONF state (R/W).

- **SPI_DIN6_NUM (for SPI2 only):** Configure the delays to input data bit6 signal based on the setting of SPI_DIN6_MODE.
  - Can be configured in CONF state.

- **SPI_DIN7_NUM (for SPI2 only):** Configure the delays to input data bit7 signal based on the setting of SPI_DIN7_MODE. 
  - Can be configured in CONF state.


**Footer:**
- Page number: 1169
- Document version and source information:
  - ESP32-S3 TRM (Version 1.7)
  - Espressif Systems

**Link:** Submit Documentation Feedback