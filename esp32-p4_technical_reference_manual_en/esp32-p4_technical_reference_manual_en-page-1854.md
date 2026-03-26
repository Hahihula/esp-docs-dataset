

```markdown
In dual stream mode, the frame order of H264 processing is fixed as A1, B1, A2, B2, A3, B3, etc. When processing frames in video sequence A, registers with the prefix H264_A_ will be automatically applied. When processing frames in video sequence B, registers with the prefix H264_B_ will be automatically applied. The registers with other prefixes are valid for both video sequence frames.

The configuration process of dual stream mode is as follows:

1. Configure ENC_CORE according to the required function:
   (a) Configure dual stream mode: Set register H264_FRAME_MODE to 1, and set register H264_DUAL_STREAM_MODE to 1.
   (b) Configure GOP (the GOP configuration of video sequence A and B must be the same): Configure the register H264_GOP_NUM as n, indicating that a GOP contains n pictures. When the register is configured as 0, the first frame of a GOP is an I frame, and the subsequent frames of a GOP are always P frames until the encoder is reset.
   (c) Configure the MB resolution of a picture: Configure the register H264_A_SYS_TOTAL_MB_X as the number of MBs in the horizontal direction of the video sequence A, and configure the register H264_A_SYS_TOTAL_MB_Y as the number of MBs in the vertical direction of the video sequence A. Configure the register H264_B_SYS_TOTAL_MB_X as the number of MBs in the horizontal direction of the video sequence B, and configure the register H264_B_SYS_TOTAL_MB_Y as the number of MBs in the vertical direction of the video sequence B. The number of MBs in the horizontal direction is equal to the width of the video divided by 16 and rounded up. And the number of MBs in the vertical direction is equal to the height of the video divided by 16 and rounded up.
   (d) Configure the initial QP of a picture: Configure the register H264_A_QP as the initial QP of video sequence A, ranging from 10 to 51. Configure the register H264_B_QP as the initial QP of video sequence B, ranging from 10 to 51.
   (e) Configure the deblocking filter: Set the register H264_A_BYPASS_DB_FILTER to 0 to enable the deblocking filter of video sequence A. Set the register H264_A_BYPASS_DB_FILTER to 1 to disable the deblocking filter of video sequence A. Set the register H264_B_BYPASS_DB_FILTER to 0 to enable the deblocking filter of video sequence B. Set the register H264_B_BYPASS_DB_FILTER to 1 to disable the deblocking filter of video sequence B.
   (f) Configure slice header information: According to the information required to be included in the slice header in the H264 standard, configure the relevant registers H264_SLICE_RMEAIN_BIT, H264_SLICE_REMAIN_BITLENGTH, H264_SLICE_BYTE_LENGTH, H264_SLICE_BYTE_LSB, and H264_SLICE_BYTE_MSB. For example, if the slice header is a variable with 41 bits and the highest significant bit is the slice header first bit, these registers should be set in the following ways.
      *   H264_SLICE_BYTE_MSB: From bit 41 to bit 10 of the slice header
      *   H264_SLICE_BYTE_LSB: From bit 9 to bit 2 of the slice header
      *   H264_SLICE_RMEAIN_BIT: Bit 1 of the slice header
      *   H264_SLICE_BYTE_LENGTH: 5
      *   H264_SLICE_BYTE_REMAIN_BITLENGTH: 1
   (g) To use the quantization result decimate function, configure its related registers referring to section 39.5.1.2.
```