

```markdown
Chapter 39 H264 Encoder

Register 39.46. H264_CONF_REG (0x0000)

H264_CLK_EN Configures whether to enable the register clock gate.
O: Enable the clock gate only when application writes registers
1: Force enable the clock gate for register
(R/W)

Register 39.47. H264_MV_MERGE_CONFIG_REG (0x0004)

H264_MV_MERGE_TYPE Configures MV merge type.
O: Merge p16x16 mv
1: Merge min mv
2: Merge max mv
3: Not valid
(R/W)

H264_INT_MV_OUT_EN Configures the output type of the merged MV.
O: Output the merged MV where any part (integer and fractional) is not zero
1: Output the merged MV where the integer part is not zero
(R/W)

H264_A_MV_MERGE_EN Configures whether to enable MV merge for video sequence A.
O: Disable
1: Enable
(R/W)

H264_B_MV_MERGE_EN Configures whether to enable MV merge for video sequence B.
O: Disable
1: Enable
(R/W)

H264_MB_VALID_NUM Represents the number of MBs in the output that contains valid merged
MVs. (RO)
```