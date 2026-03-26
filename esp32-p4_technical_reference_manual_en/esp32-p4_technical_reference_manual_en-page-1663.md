
```markdown
| Name                                 | Description                                                                                   | Address   | Access |
|--------------------------------------|-----------------------------------------------------------------------------------------------|-----------|--------|
| ISP_HIST_SEG1_REG                    | HIST X coordinate interval configuration register 1                                         | 0x01B8    | R/W    |
| ISP_HIST_SEG2_REG                    | HIST X coordinate interval configuration register 2                                         | 0x01BC    | R/W    |
| ISP_HIST_SEG3_REG                    | HIST X coordinate interval configuration register 3                                         | 0x01C0    | R/W    |
| ISP_HIST_WEIGHTO_REG                 | HIST sub-window weight configuration register 0                                              | 0x01C4    | R/W    |
| ISP_HIST_WEIGHT1_REG                 | HIST sub-window weight configuration register 1                                              | 0x01C8    | R/W    |
| ISP_HIST_WEIGHT2_REG                 | HIST sub-window weight configuration register 2                                              | 0x01CC    | R/W    |
| ISP_HIST_WEIGHT3_REG                 | HIST sub-window weight configuration register 3                                              | 0x01D0    | R/W    |
| ISP_HIST_WEIGHT4_REG                 | HIST sub-window weight configuration register 4                                              | 0x01D4    | R/W    |
| ISP_HIST_WEIGHT5_REG                 | HIST sub-window weight configuration register 5                                              | 0x01D8    | R/W    |
| ISP_HIST_WEIGHT6_REG                 | HIST sub-window weight configuration register 6                                              | 0x01DC    | R/W    |
| ISP_YUV_FORMAT_REG                   | YUV format control register                                                                  | 0x0234    | R/W    |
| ISP_CROP_CTRL_REG                    | CROP control register                                                                        | 0x0244    | WT     |
| ISP_CROP_Y_CAPTURE_REG               | CROP Y direction control register                                                            | 0x0248    | R/W    |
| ISP_CROP_X_CAPTURE_REG               | CROP X direction control register                                                            | 0x024C    | R/W    |
| ISP_CROP_ERR_ST_REG                  | CROP error status register                                                                    | 0x0250    | RO     |
| ISP_WBG_COEF_R_REG                   | WBG R channel gain register                                                                   | 0x0254    | R/W    |
| ISP_WBG_COEF_G_REG                   | WBG G channel gain register                                                                   | 0x0258    | R/W    |
| ISP_WBG_COEF_B_REG                   | WBG B channel gain register                                                                   | 0x025C    | R/W    |
| ISP_COLOR_HUE_CTRL_REG               | Hue control register                                                                          | 0x0260    | R/W    |
| ISP_AWB_BX_REG                       | AWB sub-window X direction control register                                                   | 0x0264    | R/W    |
| ISP_AWB_BY_REG                       | AWB sub-window Y direction control register                                                   | 0x0268    | R/W    |
| ISP_STATE_REG                        | ISP state register                                                                            | 0x026C    | RO     |
| ISP_SHADOW_REG_CTRL_REG              | Shadow register control register                                                              | 0x0270    | R/W    |

Status Registers
| Name                                 | Description                                                                                   | Address   | Access |
|--------------------------------------|-----------------------------------------------------------------------------------------------|-----------|--------|
| ISP_DPC_DEADPIX_CNT_REG             | DPC static calibration defective pixel number register                                       | 0x0044    | RO     |
| ISP_LUT_RDATA_REG                    | LUT read register                                                                             | 0x0050    | RO     |
| ISP_AE_BLOCK_MEAN_O_REG              | AE statistics register 0                                                                      | 0x00D8    | RO     |
| ISP_AE_BLOCK_MEAN_1_REG              | AE statistics register 1                                                                      | 0x00DC    | RO     |
| ISP_AE_BLOCK_MEAN_2_REG              | AE statistics register 2                                                                      | 0x00EO    | RO     |
| ISP_AE_BLOCK_MEAN_3_REG              | AE statistics register 3                                                                      | 0x00E4    | RO     |
| ISP_AE_BLOCK_MEAN_4_REG              | AE statistics register 4                                                                      | 0x00E8    | RO     |
| ISP_AE_BLOCK_MEAN_5_REG              | AE statistics register 5                                                                      | 0x00EC    | RO     |
| ISP_AE_BLOCK_MEAN_6_REG              | AE statistics register 6                                                                      | 0x00FO    | RO     |
```