

```markdown
Register 35.2. JPEG_DQT_INFO_REG (0x0004)

| 31 | 24 | 23 | 2 | 16 | 15 | 8 | 7 | 0 |
|----:|----:|----:|:-:|---:|---:|:-:|:-:|--|
|   3 |    |    |   |    |    |   |   |Reset|

JPEG_TO_DQT_INFO Configures quantization coefficient table0's precision and ID for decoder.
Bit[7:4]: Configures precision
Bit[3:0]: Configures ID
(R/W)

JPEG_T1_DQT_INFO Configures quantization coefficient table1's precision and ID for decoder. See details in JPEG_TO_DQT_INFO. (R/W)

JPEG_T2_DQT_INFO Configures quantization coefficient table2's precision and ID for decoder. See details in JPEG_TO_DQT_INFO. (R/W)

JPEG_T3_DQT_INFO Configures quantization coefficient table3's precision and ID for decoder. See details in JPEG_TO_DQT_INFO. (R/W)
```

```markdown
Register 35.3. JPEG_PIC_SIZE_REG (0x0008)

| 31 | 16 | 15 | 0 |
|----:|----:|---:|--|
|    |   640| 480|Reset|

JPEG_VA Configures the image's height.
When JPEG Codec works as an encoder, the maximum configurable bits is 14.
When JPEG Codec works as a decoder, the maximum configurable bits is 16.
(R/W)

JPEG_HA Configures the image's width.
When JPEG Codec works as an encoder, the maximum configurable bits is 14.
When JPEG Codec works as a decoder, the maximum configurable bits is 16.
(R/W)
```