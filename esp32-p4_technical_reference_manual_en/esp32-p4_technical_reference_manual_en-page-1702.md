

```markdown
Register 36.55. ISP_DMA_RAW_DATA_REG (0x0110)

ISP_DMA_RAW_NUM_TOTAL_SET Configures whether to update the configuration for ISP_DMA_RAW_NUM_TOTAL.
O: Not update
1: Update
(WT)
```

```markdown
Register 36.56. ISP_CAM_CNTL_REG (0x0114)

ISP_CAM_EN Configures whether to enable the input via the DVP interface.
O: Disable
1: Enable
(R/W)

ISP_CAM_UPDATE_REG Configures whether to update the configuration for ISP_CAM_CONF_REG.
O: Not update
1: Update
(R/W)

ISP_CAM_RESET Configures whether to reset the DVP input configuration.
O: Not reset
1: Reset
(R/W)

ISP_CAM_CLK_INV Configures whether to invert the DVP clock.
O: Not invert
1: Invert
(R/W)
```