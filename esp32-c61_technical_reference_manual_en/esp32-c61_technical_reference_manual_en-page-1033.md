

```markdown
## 28.9.1.2 Endian Control of Channel Valid Data

When I2S reads data through GDMA, the data endian under various data width is controlled by `I2S_TX_BIG_ENDIAN`. Table 28.9-2 shows how `I2S_TX_BIG_ENDIAN` controls the reading of the data with different valid data widths of the channel.

Table 28.9-2. Endian of Channel Valid Data

| Channel Valid Data Width | Original Data       | Endian of Processed Data                     | I2S_TX_BIG_ENDIAN |
|--------------------------|---------------------|----------------------------------------------|-------------------|
| 32                       | {B3, B2, B1, B0}    | {B3, B2, B1, B0}                             | 0                 |
|                          |                     | {BO, B1, B2, B3}                            | 1                 |
| 24                       | {B2, B1, B0}        | {B2, B1, B0}                                | 0                 |
|                          |                     | {BO, B1, B2}                                | 1                 |
| 16                       | {B1, B0}            | {B1, B0}                                    | 0                 |
|                          |                     | {BO, B1}                                    | 1                 |
| 8                        | {BO}                | {BO}                                        | x                 |

**Note:**
B0, B1, B2, B3 each represents an 8-bit data, and the symbol {} indicates that the bytes are combined together. For example, {B3, B2, B1, B0} represents a 32-bit data, wherein B0 represents bit 0-7, B1 represents bit 8-15, B2 represents bit 16-23, and B3 represents bit 24-31.

## 28.9.1.3 A-law/μ-law Compression and Decompression

ESP32-C61 I2S compresses/decompresses the valid data into 32-bit by A-law or by μ-law. If the bit width of valid data is smaller than 32, zeros are filled to the extra high bits of the data to be compressed/decompressed by default.

**Note:**
Extra high bits here mean the bits[31: channel valid data width] of the data to be compressed/decompressed.

Configure `I2S_TX_PCM_BYPASS`:
*   0: Compress or decompress the data
*   1: Do not compress or decompress the data

Configure `I2S_TX_PCM_CONF`:
*   0: Decompress the data using A-law
*   1: Compress the data using A-law
*   2: Decompress the data using μ-law
*   3: Compress the data using μ-law

At this point, the first phase of data format control is completed.
```