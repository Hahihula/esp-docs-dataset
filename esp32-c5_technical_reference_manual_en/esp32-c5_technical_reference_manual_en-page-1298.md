

```markdown
| Channel Storage Data Width | I2S_RX_BITS_MOD | I2S_RX_24_FILL_EN |
|-----------------------------|-----------------|-------------------|
| 32                          | 31              | x                 |
|                             | 23              | 1                 |
| 24                          | 23              | 0                 |
| 16                          | 15              | x                 |
| 8                           | 7               | x                 |

### 35.10.2.3 Bit Width Control of Channel RX Data

The RX data width in each channel is determined by `I2S_RX_TDM_CHAN_BITS`.

*   If the storage data width in each channel is smaller than the received (RX) data width, then only the bits within the storage data width is saved into memory. Configure `I2S_RX_LEFT_ALIGN` to:
    *   0: Only the lower bits of the received data within the storage data width is stored to memory;
    *   1: Only the higher bits of the received data within the storage data width is stored to memory.
*   If the received data width is smaller than the storage data width in each channel, the higher bits of the received data will be filled with zeros and then the data is saved to memory.

### 35.10.2.4 Endian Control of Channel Storage Data

The received data is then converted into storage data (to be stored to memory) after some processing, such as discarding extra bits or filling zeros in missing bits. The endian of the storage data is controlled by `I2S_RX_BIG_ENDIAN` under various data width. See the table below.

Table 35.10-2. Channel Storage Data Endian

| Channel Storage Data Width | Original Data   | Endian of Processed Data                     | I2S_RX_BIG_ENDIAN |
|----------------------------|-----------------|----------------------------------------------|-------------------|
| 32                         | {B3, B2, B1, B0} | {B3, B2, B1, B0}                             | 0                 |
|                            |                 | {B0, B1, B2, B3}                             | 1                 |
| 24                         | {B2, B1, B0}    | {B2, B1, B0}                                 | 0                 |
|                            |                 | {B0, B1, B2}                                 | 1                 |
| 16                         | {B1, B0}        | {B1, B0}                                     | 0                 |
|                            |                 | {B0, B1}                                     | 1                 |
| 8                          | {B0}            | {B0}                                         | x                 |

### 35.10.2.5 A-law/μ-law Compression and Decompression

ESP32-C5 I2S compresses/decompresses the storage data in 32-bit by A-law or by μ-law. By default, zeros are filled into high bits.

Configure `I2S_RX_PCM_BYPASS`:
```