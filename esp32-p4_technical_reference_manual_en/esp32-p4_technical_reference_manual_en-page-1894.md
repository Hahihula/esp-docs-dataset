

```markdown
Chapter 39 H264 Encoder

Register 39.40. H264_B_ROI_CONFIG_REG (0x009C)

H264_B_ROI_EN Configures whether to enable ROI in video sequence B.
O: Disable ROI
1: Enable ROI
(R/W)

H264_B_ROI_MODE Configures the mode of ROI in video sequence B.
O: Fixed QP
1: Delta QP
(R/W)

Register 39.41. H264_SLICE_HEADER_REMAIN_REG (0x00AC)

H264_SLICE_REMAIN_BITLENGTH Configures slice header remain bit number. (R/W)
H264_SLICE_REMAIN_BIT Configures slice header remain bit. (R/W)

Register 39.42. H264_SLICE_HEADER_BYTE_LENGTH_REG (0x00BO)

H264_SLICE_BYTE_LENGTH Configures slice header byte number. (R/W)
```