

```markdown
| Name | Description | Address | Access |
|:-------------------------------|:--------------------------------------------------------------------------|:---------|:--------|
| RX control and configuration registers |  |  |  |
| LP_I2S_RX_MEM_CONF_REG | LP I2S memory configuration register | 0x0008 | varies |
| LP_I2S_RX_CONF_REG | LP I2S RX configuration register | 0x0020 | varies |
| LP_I2S_RX_CONF1_REG | LP I2S RX configuration register 1 | 0x0028 | R/W |
| LP_I2S_RX_TDM_CTRL_REG | LP I2S RX TDM mode configuration register | 0x0050 | R/W |
| LP_I2S_RXEOF_NUM_REG | LP I2S RX data number control register | 0x0064 | R/W |
| LP_I2S_RX_PDM_CONF_REG | LP I2S RX PDM mode configuration register | 0x0070 | R/W |
| Interrupt registers |  |  |  |
| LP_I2S_INT_RAW_REG | LP I2S interrupt raw register | 0x000C | RO/WTC/SS |
| LP_I2S_INT_ST_REG | LP I2S interrupt status register | 0x0010 | RO |
| LP_I2S_INT_ENA_REG | LP I2S interrupt enable register | 0x0014 | R/W |
| LP_I2S_INT_CLR_REG | LP I2S interrupt clear register | 0x0018 | WT |
| RX clock and timing register |  |  |  |
| LP_I2S_RX_TIMING_REG | LP I2S RX timing control register | 0x0058 | R/W |
| Control and configuration registers |  |  |  |
| LP_I2S_LC_HUNG_CONF_REG | LP I2S timeout configuration register | 0x0060 | R/W |
| LP_I2S_CONF_SIGLE_DATA_REG | LP I2S single data register | 0x0068 | R/W |
| Clock register |  |  |  |
| LP_I2S_CLK_GATE_REG | Clock gate register | 0x00F8 | R/W |
| Version register |  |  |  |
| LP_I2S_DATE_REG | Version control register | 0x00FC | R/W |
```