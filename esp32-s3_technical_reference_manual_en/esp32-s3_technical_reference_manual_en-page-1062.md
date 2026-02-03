**Chapter Title:**
Chapter 28 I2S Controller (I2S)

**Register Information:**
- Register Name: `I2S_RX_CONF_REG`
- Offset: `0x0020`

**Table Description with Binary and Hexadecimal Values for Each Bit Field in the Register:**

| Bit Number | Binary Value | Hexadecimal Value |
|------------|--------------|-------------------|
| 31         | 0            | 0                 |
| ...        | ...          | ...               |
| 2           | 0            | 0                 |
| 1           | 0            | 0                 |
| ...        | ...          | ...               |
| 0           | 0            | 0                 |

**Bit Fields and Their Descriptions:**

- **I2S_RX_RESET**: Set this bit to reset RX unit. (WT)
- **I2S_RX_FIFO_RESET**: Set this bit to reset RX FIFO. (WT)
- **I2S_RX_START**: Set this bit to start receiving data. (R/W)
- **I2S_RX_SLAVE_MOD**: Set this bit to enable slave RX mode. (R/W)
- **I2S_RX_MONO**: Set this bit to enable RX unit in mono mode. (R/W)
- **I2S_RX_BIG_ENDIAN**: I2S RX byte endian: 1: low address data is saved to high address, 0: low address data is saved to low address. (R/W)
- **I2S_RX_UPDATE**: Set 1 to update I2S RX registers from APB clock domain to I2S RX clock domain.
  - This bit will be cleared by hardware after register update is done. (R/W/SC)
- **I2S_RX_MONO_FST_VLD**: The first channel data value is valid in I2S RX mono mode: 
  - `1`: First the second channel data value
  - `0`: Second, then the third.
- **I2S_RX_PCM_CONF**: I2S RX compress/decompress configuration bit:
  - `(itoa): A-Law compress`
  - `(utol): Mu-Law decompress`
  - `(ltou): Mu-Law compress` (R/W)
- **I2S_RX_BYPASS**: Set this bit to bypass Compress/Decompress module for received data. 
  - `(R/W)`
- **I2S_RX_STOP_MODE**: `0`: I2S RX stops only when I2S_RX_START is cleared.
  - `1`: I2S RX stops when
    - `I2S_RX_START` is 0 or in_suc_eof is 1. 
    - `R/W`
- **I2S_RX_LEFT ALIGN**: `1`: I2S RX left alignment mode: 
  - `0`: I2S RX right alignment mode.
- **I2S_RX_24_FILL_EN**: Store 24-bit channel data to 32 bits (Extra bits are filled with zeros): 
  - `0`: store
    - `24-bit` channel data to `24 bits`.
- **I2S_RX_WS_IDLE_POL**: WS remains low when receiving left channel data, and remains high:
  - When receiving right channel data.
  - `1`: WS remains high: 
    - Receiving received left channel data
    - Remains (`R/W`)
- **I2S_RX_BIT_ORDER**: Configures whether to reverse the bit order of I2S RX data to be received. 
  - `0`: Not reverse, `1`: Reverse (R/W)

**Footer:**
Continued on the next page...

**Document Information:**
Espressif Systems
Page Number: 1062
Document Title: ESP32-S3 TRM (Version 1.7)
Feedback Link: Submit Documentation Feedback