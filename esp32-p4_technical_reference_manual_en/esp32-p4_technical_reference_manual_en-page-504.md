

```markdown
| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| EFUSE_RD_RS_ERR1_REG                       | Programming error record register 1 for BLOCK1-10                                              | 0x01C4    | RO     |

eFuse Clock Register
| EFUSE_CLK_REG                              | eFuse clock configuration register                                                             | 0x01C8    | R/W    |

eFuse Configuration Registers
| EFUSE_CONF_REG                             | Configures eFuse operation mode                                                                 | 0x01CC    | R/W    |
| EFUSE_DAC_CONF_REG                         | Configures the eFuse programming voltage                                                        | 0x01E8    | R/W    |
| EFUSE_RD_TIM_CONF_REG                      | Configures read timing parameters                                                               | 0x01EC    | R/W    |
| EFUSE_WR_TIM_CONF1_REG                     | Configures eFuse programming timing parameters                                                 | 0x01F0    | R/W    |
| EFUSE_WR_TIM_CONF2_REG                     | Configures eFuse programming timing parameters                                                 | 0x01F4    | R/W    |
| EFUSE_WR_TIM_CONFO_RS_BYPASS_REG           | Configures eFuse programming time parameters and RS bypass operation                            | 0x01F8    | varies |

eFuse Status Register
| EFUSE_STATUS_REG                           | eFuse status register                                                                           | 0x01DO    | RO     |

eFuse Command Registers
| EFUSE_CMD_REG                              | eFuse command register                                                                          | 0x01D4    | varies |

eFuse Interrupt Registers
| EFUSE_INT_RAW_REG                          | eFuse raw interrupt register                                                                    | 0x01D8    | R/SS/W |
| EFUSE_INT_ST_REG                           | eFuse interrupt status register                                                                 | 0x01DC    | RO     |
| EFUSE_INT_ENA_REG                          | eFuse interrupt enable register                                                                 | 0x01EO    | R/W    |
| EFUSE_INT_CLR_REG                          | eFuse interrupt clear register                                                                  | 0x01E4    | WT     |

eFuse Version Register
| EFUSE_DATE_REG                             | eFuse version control register                                                                  | 0x01FC    | R/W    |
```