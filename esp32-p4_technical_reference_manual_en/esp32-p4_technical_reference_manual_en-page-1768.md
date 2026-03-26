

```markdown
| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| **Configuration Registers**                |                                                                                                  |           |        |
| PPA_BLEND0_CLUT_DATA_REG                  | CLUT SRAM data read/write register of BLEND background layer                                   | 0x0000    | R/W    |
| PPA_BLEND1_CLUT_DATA_REG                  | CLUT SRAM data read/write register of BLEND foreground layer                                   | 0x0004    | R/W    |
| PPA_CLUT_CONF_REG                         | Configures BLEND CLUT                                                                            | 0x000C    | R/W    |
| PPA_SRM_COLOR_MODE_REG                    | Configures SRM color space                                                                       | 0x0020    | R/W    |
| PPA_BLEND_COLOR_MODE_REG                  | Configures BLEND color space                                                                    | 0x0024    | R/W    |
| PPA_SRM_BYTE_ORDER_REG                    | Configures SRM byte order                                                                        | 0x0028    | R/W    |
| PPA_BLEND_BYTE_ORDER_REG                  | Configures BLEND byte order                                                                      | 0x002C    | R/W    |
| PPA_BLEND_TRANS_MODE_REG                  | Configures the BLEND mode                                                                        | 0x0034     | varies |
| PPA_SRM_FIX_ALPHA_REG                     | Configures SRM Alpha channel                                                                     | 0x0038    | R/W    |
| PPA_BLEND_TX_SIZE_REG                     | Configures BLEND image filling size                                                             | 0x003C    | R/W    |
| PPA_BLEND_FIX_ALPHA_REG                   | Configures BLEND Alpha override                                                                  | 0x0040    | R/W    |
| PPA_BLEND_RGB_REG                         | Configures RGB color                                                                             | 0x0048    | R/W    |
| PPA_BLEND_FIX_PIXEL_REG                   | Configures BLEND image filling pixel                                                            | 0x004C    | R/W    |
| PPA_CK_FG_LOW_REG                          | Configures the foreground color-key lower threshold of BLEND                                    | 0x0050    | R/W    |
| PPA_CK_FG_HIGH_REG                         | Configures the foreground color-key higher threshold of BLEND                                   | 0x0054    | R/W    |
| PPA_CK_BG_LOW_REG                          | Configures the background color-key lower threshold of BLEND                                    | 0x0058    | R/W    |
| PPA_CK_BG_HIGH_REG                         | Configures the background color-key higher threshold of BLEND                                   | 0x005C    | R/W    |
| PPA_CK_DEFAULT_REG                         | Configures the default color-key value of BLEND                                               | 0x0060    | R/W    |
| PPA_SRM_SCAL_ROTATE_REG                   | Configures the SRM mode                                                                          | 0x0064     | varies |
| PPA_SRM_MEM_PD_REG                         | Configures SRM memory                                                                            | 0x0068    | R/W    |
| PPA_REG_CONF_REG                           | Enables register clock                                                                           | 0x006C    | R/W    |
| PPA_RGB2GRAY_REG                            | Configures the coefficient in RGB to GRAY conversion                                          | 0x0098    | R/W    |
| **Interrupt Registers**                   |                                                                                                  |           |        |
| PPA_INT_RAW_REG                            | Raw status interrupt                                                                             | 0x0010     | R/ WTC/ SS |
| PPA_INT_ST_REG                              | Masked interrupt                                                                                 | 0x0014     | RO      |
| PPA_INT_ENA_REG                             | Interrupt enable bits                                                                            | 0x0018     | R/W     |
```