

```markdown
| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| **Configuration Registers**                |                                                                                                  |           |        |
| LP_ANA_BOD_MODEO_CNTL_REG                 | Brownout detector mode 0 configuration register                                                 | 0x0000    | R/W    |
| LP_ANA_BOD_MODE1_CNTL_REG                 | Brownout detector mode 1 configuration register                                                 | 0x0004    | R/W    |
| LP_ANA_POWER_GLITCH_CNTL_REG              | Voltage glitch configuration register                                                            | 0x0008    | R/W    |
| LP_ANA_FIB_ENABLE_REG                     | Voltage glitch detectors' enable control register                                                | 0x000C    | R/W    |
| LP_ANA_INT_RAW_REG                        | LP_ANA_BOD_MODEO_INT raw interrupt                                                               | 0x0010    | R/WTC/SS|
| LP_ANA_INT_ST_REG                          | LP_ANA_BOD_MODEO_INT state interrupt                                                             | 0x0014    | RO     |
| LP_ANA_INT_ENA_REG                         | LP_ANA_BOD_MODEO_INT enable register                                                             | 0x0018    | R/W    |
| LP_ANA_INT_CLR_REG                         | LP_ANA_BOD_MODEO_INT clear register                                                              | 0x001C    | WT     |
| LP_ANA_LP_INT_RAW_REG                      | LP_ANA_BOD_MODEO_LP_INT raw interrupt                                                            | 0x0020    | R/WTC/SS|
| LP_ANA_LP_INT_ST_REG                       | LP_ANA_BOD_MODEO_LP_INT state interrupt                                                          | 0x0024    | RO     |
| LP_ANA_LP_INT_ENA_REG                      | LP_ANA_BOD_MODEO_LP_INT enable register                                                          | 0x0028    | R/W    |
| LP_ANA_LP_INT_CLR_REG                      | LP_ANA_BOD_MODEO_LP_INT clear register                                                           | 0x002C    | WT     |
| **Version Control Registers**              |                                                                                                  |           |        |
| LP_ANA_DATE_REG                            | Version control register                                                                         | 0x03FC    | R/W    |
```