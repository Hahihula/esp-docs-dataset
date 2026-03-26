

```markdown
## 36.6 Interrupts

ESP32-P4’s ISP can generate the following interrupt signals that will be sent to the **Interrupt Matrix**.

- `isp_interrupt`
- `csi_bridge_interrupt`

There are several internal interrupt sources from ISP that can generate the above interrupt signal. The interrupt sources from ISP are listed with their trigger conditions and the resulted interrupt signal in Table 36.6-1.
```

```markdown
Table 36.6-1. ISP’s Internal Interrupt Sources

| Internal Interrupt Source | Trigger Condition                                                                                      | Interrupt Signal   |
|----------------------------|--------------------------------------------------------------------------------------------------------|--------------------|
| `ISP_CROP_ERR_INT`         | When the crop module window is configured incorrectly                                                  | `isp_interrupt`    |
| `ISP_WBG_FRAME_INT`        | After module WBG processes a frame                                                                    | `isp_interrupt`    |
| `ISP_CROP_FRAME_INT`       | After module crop processes a frame                                                                   | `isp_interrupt`    |
| `ISP_HEADER_IDI_FRAME_INT` | After MIPI-CSI inputs a frame. This interrupt is not affected by whether `ISP_MIPI_DATA_EN` is enabled | `isp_interrupt`    |
| `ISP_TAIL_IDI_FRAME_INT`   | After ISP_Tail outputs a frame                                                                         | `isp_interrupt`    |
| `ISP_YUV2RGB_FRAME_INT`    | After module YUV2RGB processes a frame                                                                | `isp_interrupt`    |
| `ISP_COLOR_FRAME_INT`      | After module contrast/hue/saturation/luminance adjustment processes a frame                           | `isp_interrupt`    |
| `ISP_SHARP_FRAME_INT`      | After module sharpen processes a frame                                                                | `isp_interrupt`    |
```