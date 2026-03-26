

```markdown
Register 36.91. ISP_HIST_WEIGHT6_REG (0x01DC)

ISP_HIST_WEIGHT_44 Configures the weight of HIST sub-window 44. Bits [7:0] are the fractional part. (R/W)


Register 36.92. ISP_YUV_FORMAT_REG (0x0234)

ISP_YUV_MODE Configures the YUV output mode.
O: ITU-R BT.601
1: ITU-R BT.709
(R/W)

ISP_YUV_RANGE Configures the YUV output range.
O: Full range (YUV2RGB)
1: Limit range (YUV_Limit)
(R/W)


Register 36.93. ISP_CROP_CTRL_REG (0x0244)

ISP_CROP_SFT_RST Configures whether to reset the CROP error status.
O: Not reset
1: Reset
(WT)
```