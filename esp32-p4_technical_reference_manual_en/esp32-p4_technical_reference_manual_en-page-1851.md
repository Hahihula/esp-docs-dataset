

```markdown
(a) Configure H264_DMA TX channel 0.
(b) Configure H264_DMA TX channel 1.
(c) Configure H264_DMA TX channel 2.
(d) Configure H264_DMA TX channel 3 and TX channel 4.
(e) Configure H264_DMA RX channel 0 and RX channel 1.
(f) Configure H264_DMA RX channel 2.
(g) Configure H264_DMA RX channel 3.
(h) Configure H264_DMA RX channel 4.
(i) Configure H264_DMA RX channel 5.

2. Configure ENC_CORE according to the required functions:

(a) Configure GOP mode: Set register `H264_FRAME_MODE` to 0 and register `H264_DUAL_STREAM_MODE` to 0.

(b) Configure the number of pictures in a GOP: Configure the register `H264_GOP_NUM` as n, indicating that a GOP contains n pictures. When the register is configured as 0, the first frame of a GOP is an I frame, and the subsequent frames of a GOP are always P frame until the encoder is reset.

(c) Configure the MB resolution of a picture: configure the register `H264_A_SYS_TOTAL_MB_X` as the number of MBs in the horizontal direction of the picture, and configure the register `H264_A_SYS_TOTAL_MB_Y` as the number of MBs in the vertical direction of the picture. The number of MBs in the horizontal direction is equal to the width of the video divided by 16 and rounded up. And the number of MBs in the vertical direction is equal to the height of the video divided by 16 and rounded up.

(d) Configure the initial QP value of a picture: configure the register `H264_A_QP` as the initial QP value, ranging from 10 to 51.

(e) Configure deblocking filter: Set register `H264_A_BYPASS_DB_FILTER` to 0 to enable the deblocking filter, set register `H264_A_BYPASS_DB_FILTER` to 1 to disable the deblocking filter.

(f) Configure slice header information: According to the information required to be included in the slice header in the H264 standard, configure the relevant registers `H264_SLICE_RMEAIN_BIT`, `H264_SLICE_REMAIN_BITLENGTH`, `H264_SLICE_BYTE_LENGTH`, `H264_SLICE_BYTE_LSB`, and `H264_SLICE_BYTE_MSB`. For example, if the slice header is a variable with 41 bits and the highest significant bit is the slice header first bit, these registers should be set in the following ways.

- `H264_SLICE_BYTE_MSB`: From bit 41 to bit 10 of the slice header
- `H264_SLICE_BYTE_LSB`: From bit 9 to bit 2 of the slice header
- `H264_SLICE_RMEAIN_BIT`: Bit 1 of the slice header
- `H264_SLICE_BYTE_LENGTH`: 5
- `H264_SLICE_BYTE_REMAIN_BITLENGTH`: 1

(g) To use the quantization result decimation function, configure its related registers referring to the description in section 39.5.1.2.
```