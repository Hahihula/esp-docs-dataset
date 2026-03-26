

```markdown
Register 39.2. H264_GOP_CONF_REG (0x0004)

H264_DUAL_STREAM_MODE Configures whether to enable dual stream mode. When this field is set to 1, H264_FRAME_MODE field must be set to 1 too.
O: Normal mode
1: Dual stream mode
(R/W)

H264_GOP_NUM Configures the frame number of one GOP.
O: The frame number of one GOP is infinite
Others: Actual frame number of one GOP
(R/W)
```

```markdown
Register 39.3. H264_A_SYS_MB_RES_REG (0x0008)

H264_A_SYS_TOTAL_MB_Y Configures video sequence A vertical MB resolution. (R/W)

H264_A_SYS_TOTAL_MB_X Configures video sequence A horizontal MB resolution. (R/W)
```