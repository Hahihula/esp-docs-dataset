**Title:**
Chapter 28 I2S Controller (I2S)

**Header:**
Register 28.14. I2S_TX_CLKM_CONF_REG (0x0034)

**Body Text and Table Description:**

- **Field Name:** I2S_TX_CLKM_DIV_NUM
  - **Description:** Integral I2S TX clock divider value.
  - **Access Mode:** Read/Write

- **Field Name:** I2S_TX_CLK_ACTIVE
  - **Description:** I2S TX unit clock enable signal.
  - **Access Mode:** Read/Write

- **Field Name:** I2S_TX_CLK_SEL
  - **Description:** Select clock clock for I2S TX unit. 
    - `0`: XTAL_CLK
    - `1`: PLL_D2_CLK
    - `2`: PLL_F160M_CLK (3: I2S_MCLK_in)
  - **Access Mode:** Read/Write

- **Field Name:** I2S_CLK_EN
  - **Description:** Set this bit to enable clock gate.
  - **Access Mode:** Read/Write

**Footer Information:**
Espressif Systems  
1070  
ESP32-S3 TRM (Version 1.7)  

**Link Texts:**
- GoBack
- Submit Documentation Feedback