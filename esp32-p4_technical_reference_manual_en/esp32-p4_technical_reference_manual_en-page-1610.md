

```markdown
- 2D DMA RX channel: `DMA2D_INLINK_ADDR_CHn`

4. Enable interrupt sources:
    - `DMA2D_OUT_INT_ENA_CHn_REG`
    - `DMA2D_IN_INT_ENA_CHn_REG`
    - `JPEG_INT_ENA_REG`

5. Start the transmission of 2D DMA channels:
    - 2D DMA TX channel: set `DMA2D_OUTLINK_START_CHn` to 1 and then to 0
    - 2D DMA RX channel: set `DMA2D_INLINK_START_CHn` to 1 and then to 0

6. Start the JPEG codec encoding by setting the `JPEG_JPEG_START` field.

7. Wait till `DMA2D_IN_SUC_EOF_CHn_INT` becomes 1, indicating that the encoded bitstream has been completely written to the memory.

### 35.7.2 JPEG Decoder

When the JPEG codec is working as a decoder, the configuration process is:

1. Activate the JPEG codec:
    - Set `HP_SYS_CLKRST_JPEG_SYS_CLK_EN` to 1 to enable the JPEG codec clock
    - Set `HP_SYS_CLKRST_RST_EN_JPEG` to 0 to release the JPEG codec system level reset.

2. Configure the JPEG codec:
    - Set `JPEG_SOFT_RST` to 1 to reset the JPEG codec, and then set `JPEG_SOFT_RST` to 0 to release the JPEG codec reset.
    - Set `JPEG_MODE` to 1 to configure the JPEG codec to be used as a decoder.
    - Enable the RST marker check following the instructions in Section 35.5.2.2, if required.
    - Configure the quantization coefficient tables by following the instructions in Section 35.5.2.3.
    - Configure the Huffman tables by following the instructions in Section 35.5.2.4.
    - Configure the width and height of the decoded image:
        - Width: write width of the decoded image to `JPEG_HA`.
        - Height: write the height of the decoded image to `JPEG_VA`.
        - According to different decoded image formats, `JPEG_HA` and `JPEG_VA` must meet the requirements of Table 35.7-3.

Table 35.7-3. JPEG Decoder `JPEG_HA` and `JPEG_VA` Configuration

| Format of Decoded Image | JPEG_HA           | JPEG_VA |
|-------------------------|-------------------|--------|
| YUV444                  | Multiples of 8    | 8      |
| YUV422                  | Multiples of 16   | 8      |
| YUV420                  | Multiples of 16   | 16     |
```