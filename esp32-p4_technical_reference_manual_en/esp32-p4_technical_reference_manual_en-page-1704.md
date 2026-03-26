

```markdown
Register 36.57. ISP_CAM_CONF_REG (0x0118)

Continued from the previous page...

ISP_CAM_VSYNC_FILTER_EN Configures whether to enable the vsync filtering.
    0: Disable
    1: Enable
    (R/W)

ISP_CAM_DE_ONLY Configures whether the DVP interface uses only DE data without HSYNC data.
    0: HSYNC is present
    1: HSYNC is not present
    (R/W)

Register 36.58. ISP_AF_CTRL0_REG (0x011C)
```

```markdown
ISP_AF_AUTO_UPDATE Configures whether to enable AF automatic statistics.
    0: Disable automatic statistics, and manual trigger is required
    1: Enable automatic statistics, and AF will perform statistics for every frame with the AF module enabled
    (R/W)

ISP_AF_MANUAL_UPDATE Configures AF manual statistics. With AF automatic statistics disabled, writing 1 triggers a statistics collection. (WT)

ISP_AF_ENV_THRESHOLD Configures the threshold for AF scene monitoring. If ISP_AF_ENV_USER_THRESHOLD_SUM or ISP_AF_ENV_USER_THRESHOLD_LUM is 0, an interrupt for scene monitoring will be triggered when the changes in sharpness or luminance exceed the product of the baseline value and this field for two consecutive times. 4 fractional bits. (R/W)

ISP_AF_ENV_PERIOD Configures the statistical interval frames for AF scene monitoring. Setting this filed to 0 disables the scene monitoring. (R/W)
```