

```markdown
- Configure the Buffer address pointer as the starting address where the encoded bitstream will be stored.
- Configure size as the number of bytes in the space to store the encoded bitstream.
- configure mod as 0, which means one-time reading of image blocks of hb × vb size.

(c) Connect 2D DMA channels to JPEG codec:

- Connect the TX channeln to the JPEG codec by configuring DMA2D_OUT_PERI_SEL_CHn to 0;
- Connect the RX channeln to the JPEG codec by configuring DMA2D_IN_PERI_SEL_CHn to 0.

(d) Reset 2D DMA channels:

- 2D DMA TX channeln: Set DMA2D_OUT_RST_CHn to 1 to reset 2D DMA TX channeln, then set DMA2D_OUT_RST_CHn to 0 to release the reset of 2D DMA TX channeln.
- 2D DMA RX channeln: Set DMA2D_IN_RST_CHn to 1 to reset 2D DMA RX channeln, then set DMA2D_IN_RST_CHn to 0 to release the reset of 2D DMA RX channeln.

(e) Select the burst length of 2D DMA channels:

- Configure DMA2D_OUT_MEM_BURST_LENGTH_CHn to select the burst length of 2D DMA TX channeln.
- Configure DMA2D_IN_MEM_BURST_LENGTH_CHn to select the burst length of 2D DMA RX channeln.

(f) Select the 2D DMA output image block size by configuring DMA2D_OUT_MACRO_BLOCK_SIZE_CHn according to the format of original image and the format of the image to be compressed. See details in Table 35.7-2:

- 0: 8x8
- 1: 16x8
- 2: 16x16

Table 35.7-2. DMA2D_OUT_MACRO_BLOCK_SIZE_CHn Configuration

| Format of Original Image | Format of the Image to be Compressed | DMA2D_OUT_MACRO_BLOCK_SIZE_CHn |
|--------------------------|--------------------------------------|-------------------------------|
| RGB/YUV444               | YUV444                               | 0                             |
|                          | YUV422                               | 1                             |
|                          | YUV420                               | 2                             |
| YUV422                   | YUV422                               | 1                             |
|                          | YUV420                               | 2                             |
| YUV420                   | YUV420                               | 2                             |
| GRAY                     | GRAY                                 | 0                             |

(g) Enable the reorder function to improve bandwidth utilization by setting DMA2D_OUT_REORDER_EN_CHO to 1. Note that, this function is only available for 2D DMA TX channel0, not for any other TX channels.

(h) Configure 2D DMA channel linked list address:

- 2D DMA TX channel: DMA2D_OUTLINK_ADDR_CHn
```