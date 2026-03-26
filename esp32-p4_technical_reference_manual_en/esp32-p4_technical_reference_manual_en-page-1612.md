

```markdown
- 2D DMA RX channeln: set `DMA2D_IN_RST_CHn` to 1 to reset 2D DMA RX channeln, then set `DMA2D_IN_RST_CHn` to 0 to release the reset of 2D DMA RX channeln.

(e) Select the burst length of 2D DMA channels:

- Configure `DMA2D_OUT_MEM_BURST_LENGTH_CHn` to select the burst length of 2D DMA TX channeln
- Configure `DMA2D_IN_MEM_BURST_LENGTH_CHn` to select the burst length of 2D DMA RX channeln

(f) Select 2D DMA receive image block size by configuring `DMA2D_IN_MACRO_BLOCK_SIZE_CHn` according to the format of the decoded image. See details in Table 35.7-5:

- 0: 8x8
- 1: 16x8
- 2: 16x16

Table 35.7-5. DMA2D_IN_MACRO_BLOCK_SIZE_CHn Configuration

| Format of Decoded Image | DMA2D_IN_MACRO_BLOCK_SIZE_CHn |
|-------------------------|-------------------------------|
| YUV444                  | 0                             |
| YUV422                  | 1                             |
| YUV420                  | 2                             |
| GRAY                    | 0                             |

(g) Enable the reorder function to improve bandwidth utilization by setting set `DMA2D_IN_REORDER_EN_CHO` to 1. Note that, this function is only available for 2D DMA RX channel0, not for any other RX channels.

(h) Select whether to scramble the pixel order of the decoded image before 2D DMA color space conversion by configuring `DMA2D_IN_SCRAMBLE_SEL_PRE_CHO`:

- 0: BYTE2-1-O
- 1: BYTE2-O-1
- 2: BYTE1-O-2
- 3: BYTE1-2-O
- 4: BYTEO-2-1
- 5: BYTEO-1-2

Configuring `DMA2D_IN_SCRAMBLE_SEL_PRE_CHO` to 5 means swapping the pixel order, for example, swapping YUV444 output by the JPEG decoder to VUY444. Note that, this function is only available for 2D DMA RX channel0, not for any other RX channels.

(i) Select the color conversion methods by configuring `DMA2D_IN_COLOR_INPUT_SEL_CHO`, `DMA2D_IN_COLOR_3B_PROC_EN_CHO`, and `DMA2D_IN_COLOR_OUTPUT_SEL_CHO`. See details in Table 35.7-6:
```