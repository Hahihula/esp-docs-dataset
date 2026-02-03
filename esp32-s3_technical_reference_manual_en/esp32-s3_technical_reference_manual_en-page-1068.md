**Chapter Title:**
Chapter 28 I2S Controller (I2S) Register

**Register Name and Address:**
I2S_TX_CONF_REG (0x0024)

**Table Description with Columns Labels in Markdown format:**
- **Columns:** 
  - Offset
  - Bit Range
  - Description
  
| Offset | Bit Range | Description |
|--------|-----------|-------------|
| 31     | Reserved | (reserved) |
| ...    | ...       | ...         |

**Register Details with Descriptions in Markdown format:**

- **I2S_TX_RESET**
  - Set this bit to reset TX unit. (WT)

- **I2S_TX_FIFO_RESET**
  - Set this bit to reset TX FIFO. (WT)

- **I2S_TX_START**
  - Set this bit to start transmitting data. (R/W)

- **I2S_TX_SLAVE_MOD**
  - Set this bit to enable slave TX mode. (R/W)

- **I2S_TX_MONO**
  - Set this bit to enable TX unit in mono mode. (R/W)

- **I2S_TX_CHAN_EQUAL**
  - The left channel data is equal to right channel data in I2S TX mono mode or TDM mode.
    - O: The invalid channel data is I2S_SINGLE_DATA in I2S TX mono mode or TDM mode.

- **I2S_TX_BIG_ENDIAN**
  - Set this bit for byte endian. 
    - 1: low address data is saved to high address
    - 0: low address data is saved to low address

- **I2S_TX_UPDATE**
  - Set 1 to update I2S TX registers from APB clock domain to I2S TX clock domain.
  - This bit will be cleared by hardware after register update is done. (R/W/SC)

- **I2S_TX_MONO_FST_VLD**
  - The first channel data is valid in I2S TX mono mode
    - O: The second channel data is valid in I2S TX mono mode

- **I2S_TX_PCM_CONF**
  - Set this bit to bypass Compress/Decompress module for transmitted data.
    - (R/W)

- **I2S_TX_STOP_EN**
  - Set this bit to stop outputting BCK signal and WS signal when TX FIFO is empty.

- **I2S_TX_LEFT ALIGN**
  - I2S TX left alignment mode
    - O: I2S TX right alignment mode

- **I2S_TX_24_FILL_EN**
  - Send 32 bits in 24-bit channel data mode. Extra bits are filled with zeros.
  
- **I2S_TX_WS_IDLE_POL**
  - WS remains low when sending left channel data, and remains high when sending right channel data
    - O: WS remains high

- **I2S_TX_BIT_ORDER**
  - Configures whether to reverse the bit order of valid data to be sent by I2S TX.
    - R/W
  
- **I2S_TX_TDM_EN**
  - Enable I2S TDM TX mode
    - O: Disable I2S TDM TX mode

**Footer Note:** 
Continued on the next page...

**Document Information at Bottom of Page:**
ESP32-S3 TRM (Version 1.7)
Espressif Systems