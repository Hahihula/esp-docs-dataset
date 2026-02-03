**Chapter Title:**
Chapter 28 I2S Controller (I2S)

**Table Title and Content:**
- **Table 28.9-2. Endian of Channel Valid Data**

| Width | Origin Data                   | Endian of Processed Data |
|-------|-------------------------------|---------------------------|
|       | {B3, B2, B1, BO}             | {B3, B2, B1, BO}         |
| 32    |                               | 0                         |
| 24    | {B2, B1, BO}                 | {B2, B1, BO}             |
|       |                               | 0                         |
| 16    | {B1, BO}                     | {B1, BO}                 |
|       |                               | 0                         |
| 8     | {BO}                         | {BO}                     |
|       |                               | x                         |

**Subsection Title:**
28.9.1.3 A-law/μ-law Compression and Decompression

**Body Text:**
ESP32-S3 I2S[2] compresses/decompresses the valid data into 32-bit by A-law or by μ-law. If the bit width of valid data is smaller than 32, zeros are filled to the extra high bits of the data to be compressed/decompressed by default.

**Note:**
Extra high bits here mean the bits [31: channel valid data width] of the data to be compressed/decompressed.

**Configuration Instructions for I2S_TX_PCM_BYPASS:**
- 0: Compress or decompress the data.
- 1: Do not compress or decompress the data.

**Configuration Instructions for I2S_TX_PCM_CONF:**
- 0: Decompress the data using A-law.
- 1: Compress the data using A-law.
- 2: Decompress the data using μ-law.
- 3: Compress the data using μ-law.

At this point, the first phase of data format control is complete.

**Subsection Title:**
28.9.1.4 Bit Width Control of Channel TX Data

**Body Text:**
The TX data width in each channel is determined by I2S_TX_TDM_CHAN BITS.
- If TX data width in each channel is larger than the valid data width, zeros will be filled to these extra bits.

**Configuration Instructions for I2S_TX_LEFT ALIGN:**
- 0: The valid data is at the lower bits of TX data.
- 1: The valid data is at the higher bits of TX data.

**Additional Information:**
If the TX data width in each channel is smaller than the valid data width, only the lower bits of valid data are sent out, and the higher bits are discarded. At this point, the second phase of data format control is complete.

**Footer:**
Espressif Systems
1049 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback