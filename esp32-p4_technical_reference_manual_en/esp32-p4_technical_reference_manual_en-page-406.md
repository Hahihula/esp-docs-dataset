
```markdown
Table 6.4-4. Recommended Configurations for Macroblock Reordering in TX Direction

| Byte/Pixel | Macroblock Size (Pixel) | Optimal Macroblock Count | hb | vb |
|------------|--------------------------|----------------------------|----|----|
| 3          | 8 × 8                    |                            | 5  | 40 | 8  |
| 3          | 16 × 8                   |                            | 2  | 32 | 8  |
| 3          | 16 × 16                  |                            | 2  | 32 | 16 |
| 2          | 8 × 8                    |                            | 8  | 64 | 8  |
| 2          | 16 × 8                   |                            | 4  | 64 | 8  |
| 2          | 16 × 16                  |                            | 3  | 48 | 16 |
| 1          | 8 × 8                    |                            | 16 | 128| 8  |

The macroblock size in TX direction should be configured via the DMA2D_OUT_MACRO_BLOCK_SIZE_CHn field.

6.4.6.2 Macroblock Reordering in RX Direction

Currently, in RX direction the 2D-DMA can only reorder the data decoded by JPEG (the bitstream is 1 scan, see Chapter 35 JPEG Codec). The 2D-DMA breaks down color component data decoded by JPEG into pixels, assembles them into larger macroblocks, and writes these blocks into the memory.

The data formats decoded by JPEG include GRAY, YUV444, YUV422, and YUV420. Recommended configurations for macroblock reordering are listed in Table 6.4-5.

Table 6.4-5. Recommended Configuration Table for Macroblock Reordering in 2D-DMA Receive Direction (Without Color Format Conversion)

| Format | Macroblock Size (pixels) | Optimal Macroblock Count | hb | vb |
|--------|---------------------------|----------------------------|----|----|
| GRAY   | 8 × 8                     |                            | 12 | 96 | 8  |
| YUV444 | 8 × 8                     |                            | 5  | 40 | 8  |
| YUV422 | 16 × 8                    |                            | 4  | 64 | 8  |
| YUV420 | 16 × 16                   |                            | 3  | 48 | 16 |

The macroblock size in TX direction should be configured via the DMA2D_IN_MACRO_BLOCK_SIZE_CHn field.

Figure 6.4-4 shows the layout of macroblocks outputted by the JPEG decoder. Each blue grid in this figure represents 8x8 bytes of continuous data, and for each color format the figure displays four macroblocks of 8 × 8 pixels.
```