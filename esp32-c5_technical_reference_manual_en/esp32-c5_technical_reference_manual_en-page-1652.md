

```markdown
| Name | Description | Address | Access |
|:------------------------------------------|:------------------------------------------------------------------------------------------------------------------|:---------|:-------|
| PARLIO RX Configuration Registers | | | |
| PARL_IO_RX_MODE_CFG_REG | PARLIO RX sampling mode configuration register | 0x0000 | R/W |
| PARL_IO_RX_DATA_CFG_REG | PARLIO RX data configuration register | 0x0004 | R/W |
| PARL_IO_RX_GENRL_CFG_REG | PARLIO RX general configuration register | 0x0008 | R/W |
| PARL_IO_RX_START_CFG_REG | PARLIO RX start configuration register | 0x000C | R/W |
| PARLIO TX Configuration Registers | | | |
| PARL_IO_TX_DATA_CFG_REG | PARLIO TX data configuration register | 0x0010 | R/W |
| PARL_IO_TX_START_CFG_REG | PARLIO TX start configuration register | 0x0014 | R/W |
| PARL_IO_TX_GENRL_CFG_REG | PARLIO TX general configuration register | 0x0018 | R/W |
| PARLIO Configuration and Status Registers | | | |
| PARL_IO_FIFO_CFG_REG | PARLIO FIFO configuration register | 0x001C | R/W |
| PARL_IO_REG_UPDATE_REG | PARLIO register update configuration register | 0x0020 | WT |
| PARL_IO_ST_REG | PARLIO module status register | 0x0024 | RO |
| PARLIO Interrupt Configuration and Status Registers | | | |
| PARL_IO_INT_ENA_REG | PARLIO interrupt enable signal configuration register | 0x0028 | R/W |
| PARL_IO_INT_RAW_REG | PARLIO interrupt raw signal status register | 0x002C | R/SS/WTC |
| PARL_IO_INT_ST_REG | PARLIO interrupt signal status register | 0x0030 | RO |
| PARL_IO_INT_CLR_REG | PARLIO interrupt clear signal configuration register | 0x0034 | WT |
| PARLIO RX/TX Status Registers | | | |
| PARL_IO_RX_STO_REG | PARLIO RX status register 0 | 0x0038 | RO |
| PARL_IO_RX_ST1_REG | PARLIO RX status register 1 | 0x003C | RO |
| PARL_IO_TX_STO_REG | PARLIO TX status register 0 | 0x0040 | RO |
| PARLIO Clock Configuration Registers | | | |
| PARL_IO_RX_CLK_CFG_REG | PARLIO RX clock configuration register | 0x0044 | R/W |
| PARL_IO_TX_CLK_CFG_REG | PARLIO TX clock configuration register | 0x0048 | R/W |
| PARL_IO_CLK_REG | PARLIO clock configuration register | 0x0120 | R/W |
| PARLIO Version Register | | | |
| PARL_IO_VERSION_REG | Version control register | 0x03FC | R/W |
```