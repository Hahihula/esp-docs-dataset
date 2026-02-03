**Chapter Title:**
Chapter 28 I2S Controller (I2S)

**Navigation Link:**
GoBack

---

**Continuation Note:**
Continued from the previous page...

**Register Description and Details for Register 28.12 - I2S_TX_CONF_REG (0x0024):**

- **I2S_TX_PDM_EN**: 
  - Description: Enable I2S PDM TX mode.
  - Value Range: 0: Disable, 1: Enable
  - Access Type: Read/Write

- **I2S_TX_CHAN_MOD**:
  - Description: I2S TX channel configuration bits. For more information, see Table 28.9-4 (R/W)

- **I2S_SIG_LOOPBACK**:
  - Description: Enable signal loop back mode with TX unit and RX unit sharing the same WS and BCK signals.
  - Access Type: Read/Write

---

**Register Description for Register 28.13 - I2S_TX_CONF1_REG (0x002C):**

- **I2S_TX_BCK_NO_DLY**: 
  - Description: Not specified in the image.

- **I2S_TX_MSB_SHIFT**:
  - Description: Not specified in the image.
  
- **I2S_TX_CHAN BITS**:
  - Description: Configure TX bit number for each channel in TDM mode. Bit number expected = this value + 1 (R/W)

- **I2S_TX_DTM_CHAN BITS**:
  - Description: Not specified in the image.

- **I2S_TX_BCK_NO_DLY**:
  - Description: BCK is not delayed to generate rising/falling edge in master mode. O: BCK is delayed to generate rising/falling edge in master mode (R/W)

---

**Detailed Register Descriptions for I2S_TX_CONF1_REG (0x002C):**

- **I2S_TX_TDM_WS_WIDTH**: 
  - Description: The width of tx_ws_out (WS default level) in TDM mode is (I2S_TX_TDM_WS_WIDTH + 1) * T_BCK.
  - Access Type: Read/Write

- **I2S_TX_BCK_DIV_NUM**:
  - Description: Configure the divider of BCK in TX mode. Note this divider must not be configured to 1.
  - Access Type: Read/Write
  
- **I2S_TX BITS_MOD**: 
  - Description: Set the bits to configure valid data bit length of I2S TX channel (7, all the valid channel data is in 8-bit mode; 15, all the valid channel data is in 16-bit mode; 23, all the valid channel data is in 24-bit mode; 31, all the valid channel data is in 32-bit mode).
  - Access Type: Read/Write

- **I2S_TX_HALF_SAMPLE BITS**:
  - Description: I2S TX half sample bits. This value x 2 is equal to the BCK cycles in one WS period.
  - Access Type: Read/Write
  
- **I2S_TX_MSB_SHIFT**: 
  - Description: Control the timing between WS signal and the MSB of data (1, WS signal changes one BCK clock earlier; O, Align at rising edge).
  - Access Type: Read/Write

---

**Footer Information:**
Espressif Systems
Submit Documentation Feedback
ESP32-S3 TRM (Version 1.7)