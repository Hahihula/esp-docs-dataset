

```markdown
Register 36.159. CSI_BRIG_HOST_SIZE_CTRL_REG (0x004C)

| Bit Range | Field Name                     | Description                                                                 |
|-----------|---------------------------------|-----------------------------------------------------------------------------|
| 31        | (reserved)                     |                                                                             |
| 12..11    | CSI_BRIG_CSI_HOST_CM_VNUM      |                                                                             |
| 0         |                                | Reset                                                                       |

CSI_BRIG_CSI_HOST_CM_HNUM Configures the horizontal size of the MIPI CSI input image interface (in units of 32-bit data). The value is line_pix_num * bits_per_pix / 32 - 1, and is valid only when converting from YUV422 to YUV420. (R/W)
```