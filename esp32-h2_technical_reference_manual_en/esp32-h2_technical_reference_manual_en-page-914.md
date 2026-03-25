

```markdown
## 31.10.2.3 Bit Width Control of Channel RX Data

The RX data width in each channel is determined by `I2S_RX_TDM_CHAN_BITS`.

- If the storage data width in each channel is smaller than the received (RX) data width, then only the bits within the storage data width is saved into memory. Configure `I2S_RX_LEFT_ALIGN` to:
  - `0`: Only the lower bits of the received data within the storage data width is stored to memory;
  - `1`: Only the higher bits of the received data within the storage data width is stored to memory.
- If the received data width is smaller than the storage data width in each channel, the higher bits of the received data will be filled with zeros and then the data is saved to memory.

## 31.10.2.4 Endian Control of Channel Storage Data

The received data is then converted into storage data (to be stored to memory) after some processing, such as discarding extra bits or filling zeros in missing bits. The endian of the storage data is controlled by `I2S_RX_BIG_ENDIAN` under various data width. See the table below.

Table 31.10-2. Channel Storage Data Endian

| Channel Storage Data Width | Original Data   | Endian of Processed Data       | I2S_RX_BIG_ENDIAN |
|----------------------------|-----------------|--------------------------------|-------------------|
| 32                         | {B3, B2, B1, BO} | {B3, B2, B1, BO}               | 0                 |
|                            |                 | {BO, B1, B2, B3}               | 1                 |
| 24                         | {B2, B1, BO}    | {B2, B1, BO}                   | 0                 |
|                            |                 | {BO, B1, B2}                   | 1                 |
| 16                         | {B1, BO}        | {B1, BO}                       | 0                 |
|                            |                 | {BO, B1}                       | 1                 |
| 8                          | {BO}            | {BO}                           | x                 |

## 31.10.2.5 A-law/μ-law Compression and Decompression

ESP32-H2 I2S compresses/decompresses the storage data in 32-bit by A-law or by μ-law. By default, zeros are filled into high bits.

Configure `I2S_RX_PCM_BYPASS`:
- `0`: Compress or decompress the data
- `1`: Do not compress or decompress the data

Configure `I2S_RX_PCM_CONF`:
- `0`: Decompress the data using A-law
- `1`: Compress the data using A-law
- `2`: Decompress the data using μ-law
- `3`: Compress the data using μ-law

At this point, the data format control is completed. Data then is stored into memory via GDMA.
```