

```markdown
## Register 37.9. PPA_SRM_FIX_ALPHA_REG (0x0038)

| Bit | Description |
|-----|-------------|
| 31-12 | reserved |
| 11   | PPA_SRM_RX_ALPHA_INV |
| 10   | PPA_SRM_RX_ALPHA_MOD |
| 9    | PPA_SRM_RX_FIX_ALPHA |

PPA_SRM_RX_FIX_ALPHA Configures the Alpha channal value of SRM. (R/W)

PPA_SRM_RX_ALPHA_MOD Configures the Alpha mode of SRM input data.
1: Use the value of PPA_SRM_RX_FIX_ALPHA
2: Use the value of the higher eight bits of the original Alpha value multiplied by PPA_SRM_RX_FIX_ALPHA
Others: Use the value of the original Alpha value (R/W)

PPA_SRM_RX_ALPHA_INV Configures whether to invert the original Alpha value of SRM.
O: Not invert
1: Invert to 255 minus the original Alpha value
For data formats without Alpha channels, the original Alpha value is 255. (R/W)

## Register 37.10. PPA_BLEND_TX_SIZE_REG (0x003C)

| Bit | Description |
|-----|-------------|
| 31-28 | reserved |
| 27   | PPA_BLEND_VB |
| 14   | PPA_BLEND_HB |

PPA_BLEND_HB Configures the horizontal width of image block that would be filled in the image filling mode. Measurement unit: pixel. (R/W)

PPA_BLEND_VB Configures the vertical width of image block that would be filled in the image filling mode. Measurement unit: pixel. (R/W)
```