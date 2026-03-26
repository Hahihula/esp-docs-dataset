

```markdown
| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| **Configuration Registers**                |                                                                             |         |        |
| ISP_CLK_EN_REG                             | ISP clock control register                                                  | 0x0004  | R/W    |
| ISP_CNTL_REG                               | ISP enable register                                                         | 0x0008  | R/W    |
| ISP_HSYNC_CNT_REG                          | Hsync interval control register                                             | 0x000C  | R/W    |
| ISP_FRAME_CFG_REG                          | Image control register                                                      | 0x0010  | R/W    |
| ISP_CCM_COEFO_REG                          | CCM parameter register 0                                                    | 0x0014  | R/W    |
| ISP_CCM_COEF1_REG                          | CCM parameter register 1                                                    | 0x0018  | R/W    |
| ISP_CCM_COEF3_REG                          | CCM parameter register 3                                                    | 0x001C  | R/W    |
| ISP_CCM_COEF4_REG                          | CCM parameter register 4                                                    | 0x0020  | R/W    |
| ISP_CCM_COEF5_REG                          | CCM parameter register 5                                                    | 0x0024  | R/W    |
| ISP_BF_MATRIX_CTRL_REG                     | BF pixel-to-matrix control register                                         | 0x0028  | R/W    |
| ISP_BF_SIGMA_REG                           | BF noise reduction strength control register                                | 0x002C  | R/W    |
| ISP_BF_GAUO_REG                            | BF noise reduction template register 0                                      | 0x0030  | R/W    |
| ISP_BF_GAU1_REG                            | BF noise reduction template register 1                                      | 0x0034  | R/W    |
| ISP_DPC_CTRL_REG                           | DPC control register                                                        | 0x0038  | R/W    |
| ISP_DPC_CONF_REG                           | DPC parameter register                                                      | 0x003C  | R/W    |
| ISP_DPC_MATRIX_CTRL_REG                    | DPC pixel-to-matrix control register                                        | 0x0040  | R/W    |
| ISP_LUT_CMD_REG                            | LUT command register                                                        | 0x0048  | WT     |
| ISP_LUT_WDATA_REG                          | LUT write register                                                          | 0x004C  | R/W    |
| ISP_LSC_TABLESIZE_REG                      | LSC parameter control register                                              | 0x0054  | R/W    |
| ISP_DEMOISAIC_MATRIX_CTRL_REG              | Demosaic pixel-to-matrix control register                                    | 0x0058  | R/W    |
| ISP_DEMOISAIC_GRAD_RATIO_REG               | Demosaic parameter control register                                         | 0x005C  | R/W    |
| ISP_GAMMA_CTRL_REG                         | Gamma correction control register                                           | 0x0074  | R/W    |
| ISP_GAMMA_RY1_REG                          | Gamma curve R channel Y axis configuration register 1                       | 0x0078  | R/W    |
| ISP_GAMMA_RY2_REG                          | Gamma curve R channel Y axis configuration register 2                       | 0x007C  | R/W    |
| ISP_GAMMA_RY3_REG                          | Gamma curve R channel Y axis configuration register 3                       | 0x0080  | R/W    |
| ISP_GAMMA_RY4_REG                          | Gamma curve R channel Y axis configuration register 4                       | 0x0084  | R/W    |
| ISP_GAMMA_GY1_REG                          | Gamma curve G channel Y axis configuration register 1                       | 0x0088  | R/W    |
| ISP_GAMMA_GY2_REG                          | Gamma curve G channel Y axis configuration register 2                       | 0x008C  | R/W    |
```