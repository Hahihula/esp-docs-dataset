

```markdown
Table 30.9-1. Bit Width of Channel Valid Data

| Channel Valid Data Width | I2S_TX_BITS_MOD | I2S_TX_24_FILL_EN |
|--------------------------|------------------|-------------------|
| 32                       | 31               | x                 |
|                          | 23               | 1                 |
| 24                       | 23               | 0                 |
| 16                       | 15               | x                 |
| 8                        | 7                | x                 |

* "x" represents that this value is ignored.

## 30.9.1.2 Endian Control of Channel Valid Data

When I2S reads data through DMA, the data endian under various data width is controlled by `I2S_TX_BIG_ENDIAN`. Table 30.9-2 shows how `I2S_TX_BIG_ENDIAN` controls the data reading with different channel valid data widths.

Table 30.9-2. Endian of Channel Valid Data

| Channel Valid Data Width | Original Data   | Endian of Processed Data                     | I2S_TX_BIG_ENDIAN |
|--------------------------|-----------------|-----------------------------------------------|-------------------|
| 32                       | {B3, B2, B1, BO} | {B3, B2, B1, BO}                               | 0                 |
|                          |                 | {BO, B1, B2, B3}                               | 1                 |
| 24                       | {B2, B1, BO}     | {B2, B1, BO}                                   | 0                 |
|                          |                 | {BO, B1, B2}                                   | 1                 |
| 16                       | {B1, BO}         | {B1, BO}                                       | 0                 |
|                          |                 | {BO, B1}                                       | 1                 |
| 8                        | {BO}             | {BO}                                           | x                 |

**Note:**
B0, B1, B2, B3 each represents an 8-bit data, and the symbol {} means that the bytes are combined together. For example, {B3, B2, B1, BO} represents a 32-bit number, wherein BO represents bit 0-7, B1 represents bit 8-15, B2 represents bit 16-23, and B3 represents bit 24-31.

## 30.9.1.3 A-law/μ-law Compression and Decompression

ESP32-C6 I2S compresses/decompresses the valid data into 32-bit by A-law or by μ-law. If the bit width of valid data is smaller than 32, zeros are filled to the extra high bits of the data to be compressed/decompressed by default.

**Note:**
Extra high bits here mean the bits[31: channel valid data width] of the data to be compressed/decompressed.

Configure `I2S_TX_PCM_BYPASS`:
* 0: compress or decompress the data
* 1: do not compress or decompress the data
```