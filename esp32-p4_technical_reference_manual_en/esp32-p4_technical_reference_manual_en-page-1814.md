

```markdown
| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| **LCD Module Configuration Registers**     |                                                                                                  |           |        |
| LCD_CAM_LCD_CLOCK_REG                     | LCD clock configuration register                                                               | 0x0000    | R/W    |
| LCD_CAM_LCD_RGB_YUV_REG                   | LCD data format conversion register                                                            | 0x0010    | R/W    |
| LCD_CAM_LCD_USER_REG                      | LCD user configuration register                                                                | 0x0014    | varies |
| LCD_CAM_LCD_MISC_REG                      | LCD MISC configuration register                                                                | 0x0018    | varies |
| LCD_CAM_LCD_CTRL_REG                      | LCD signal configuration register                                                              | 0x001C    | R/W    |
| LCD_CAM_LCD_CTRL1_REG                     | LCD signal configuration register 1                                                            | 0x0020    | R/W    |
| LCD_CAM_LCD_CTRL2_REG                     | LCD signal configuration register 2                                                            | 0x0024    | R/W    |
| LCD_CAM_LCD_FIRST_CMD_VAL_REG             | LCD command value configuration register                                                      | 0x0028    | R/W    |
| LCD_CAM_LCD_LATTER_CMD_VAL_REG            | LCD command value configuration register                                                     | 0x002C    | R/W    |
| LCD_CAM_LCD_DLY_MODE_CFG1_REG             | LCD data/signal delay configuration register                                                  | 0x0030    | R/W    |
| LCD_CAM_LCD_DLY_MODE_CFG2_REG             | LCD signal delay mode configuration register                                                  | 0x0038    | R/W    |
| **Camera Module Configuration Registers** |                                                                                                  |           |        |
| LCD_CAM_CAM_CTRL_REG                      | Camera clock configuration                                                                      | 0x0004    | R/W    |
| LCD_CAM_CAM_CTRL1_REG                     | Camera control register                                                                         | 0x0008    | varies |
| LCD_CAM_CAM_RGB_YUV_REG                   | Camera data format conversion register                                                         | 0x000C    | R/W    |
| **Interrupt Registers**                   |                                                                                                  |           |        |
| LCD_CAM_LC_DMA_INT_ENA_REG                | LCD_CAM GDMA interrupt enable register                                                         | 0x0064    | R/W    |
| LCD_CAM_LC_DMA_INT_RAW_REG                | LCD_CAM GDMA raw interrupt status register                                                    | 0x0068    | RO     |
| LCD_CAM_LC_DMA_INT_ST_REG                 | LCD_CAM GDMA masked interrupt status register                                                 | 0x006C    | RO     |
| LCD_CAM_LC_DMA_INT_CLR_REG                | LCD_CAM GDMA interrupt clear register                                                         | 0x0070    | WO     |
| **Version Control Register**              |                                                                                                  |           |        |
| LCD_CAM_LC_DATE_REG                       | Version control register                                                                        | 0x00FC    | R/W    |
```