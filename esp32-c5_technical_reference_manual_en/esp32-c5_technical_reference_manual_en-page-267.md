

```markdown
| Name | Description | Address | Access |
| :------------------------------------------ | :----------------------------------------------------------------------------------------------------------------- | :------- | :------ |
| EFUSE_RD_REPEAT_DATA_ERR1_REG | Programming error record register 1 for BLOCK0 | 0x0180 | RO |
| EFUSE_RD_REPEAT_DATA_ERR2_REG | Programming error record register 2 for BLOCK0 | 0x0184 | RO |
| EFUSE_RD_REPEAT_DATA_ERR3_REG | Programming error record register 3 for BLOCK0 | 0x0188 | RO |
| EFUSE_RD_REPEAT_DATA_ERR4_REG | Programming error record register 4 for BLOCK0 | 0x018C | RO |

Error Report Registers for RS Block
| Name | Description | Address | Access |
| :------------------------------------------ | :----------------------------------------------------------------------------------------------------------------- | :------- | :------ |
| EFUSE_RD_RS_DATA_ERR0_REG | Programming error record register 0 for BLOCK1-10 | 0x0190 | RO |
| EFUSE_RD_RS_DATA_ERR1_REG | Programming error record register 1 for BLOCK1-10 | 0x0194 | RO |

eFuse Version Register
| Name | Description | Address | Access |
| :---------------------- | :----------------------------------------------------------------------------------------------------------------- | :------- | :------ |
| EFUSE_DATE_REG | eFuse version control register | 0x0198 | R/W |

eFuse Clock Register
| Name | Description | Address | Access |
| :--------------------- | :----------------------------------------------------------------------------------------------------------------- | :------- | :------ |
| EFUSE_CLK_REG | eFuse clock configuration register | 0x01C8 | R/W |

eFuse Configuration Registers
| Name | Description | Address | Access |
| :------------------------------------------ | :----------------------------------------------------------------------------------------------------------------- | :------- | :------ |
| EFUSE_CONF_REG | Configures eFuse operation mode | 0x01CC | R/W |
| EFUSE_DAC_CONF_REG | Configures the eFuse programming voltage | 0x01EC | R/W |
| EFUSE_RD_TIM_CONF_REG | Configures read timing parameters | 0x01FO | R/W |
| EFUSE_WR_TIM_CONF1_REG | Configures eFuse programming timing parameters | 0x01F4 | R/W |
| EFUSE_WR_TIM_CONF2_REG | Configures eFuse programming timing parameters | 0x01F8 | R/W |
| EFUSE_WR_TIM_CONFO_RS_BYPASS_REG | Configures register0 of eFuse programming time parameters and RS bypass operation | 0x01FC | varies |

eFuse ECDSA Configure Registers
| Name | Description | Address | Access |
| :-------------------------- | :----------------------------------------------------------------------------------------------------------------- | :------- | :------ |
| EFUSE_ECDSA_REG | eFuse status register. | 0x01DO | varies |

eFuse Status Registers
| Name | Description | Address | Access |
| :------------------------- | :----------------------------------------------------------------------------------------------------------------- | :------- | :------ |
| EFUSE_STATUS_REG | eFuse status register | 0x01D4 | RO |

eFuse Command Registers
| Name | Description | Address | Access |
| :------------------------ | :----------------------------------------------------------------------------------------------------------------- | :------- | :------ |
| EFUSE_CMD_REG | eFuse command register | 0x01D8 | varies |

eFuse Interrupt Registers
| Name | Description | Address | Access |
| :---------------------------------- | :----------------------------------------------------------------------------------------------------------------- | :------- | :------ |
| EFUSE_INT_RAW_REG | eFuse raw interrupt register | 0x01DC | R/SS/WTC |
| EFUSE_INT_ST_REG | eFuse interrupt status register | 0x01EO | RO |
| EFUSE_INT_ENA_REG | eFuse interrupt enable register | 0x01E4 | R/W |
| EFUSE_INT_CLR_REG | eFuse interrupt clear register | 0x01E8 | WT |
```