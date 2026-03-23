

```markdown
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| **Interrupt registers**                    |                                                                             |           |        |
| I2S_INT_RAW_REG                           | I2S interrupt raw register                                                  | 0x000C    | RO/WTC/SS |
| I2S_INT_ST_REG                             | I2S interrupt status register                                               | 0x0010    | RO     |
| I2S_INT_ENA_REG                            | I2S interrupt enable register                                                | 0x0014    | R/W    |
| I2S_INT_CLR_REG                            | I2S interrupt clear register                                                 | 0x0018    | WT     |
| **RX control and configuration registers** |                                                                             |           |        |
| I2S_RX_CONF_REG                           | I2S RX configuration register                                                | 0x0020    | varies |
| I2S_RX_CONF1_REG                           | I2S RX configuration register 1                                              | 0x0028    | R/W    |
| I2S_TX_PCM2PDM_CONF_REG                   | I2S TX PCM-to-PDM configuration register                                     | 0x0040    | R/W    |
| I2S_TX_PCM2PDM_CONF1_REG                  | I2S TX PCM-to-PDM configuration register 1                                   | 0x0044    | R/W    |
| I2S_RX_TDM_CTRL_REG                       | I2S TX TDM mode control register                                             | 0x0050    | R/W    |
| I2S_RXEOF_NUM_REG                         | I2S RX data number control register                                          | 0x0064    | R/W    |
| **TX control and configuration registers** |                                                                             |           |        |
| I2S_TX_CONF_REG                           | I2S TX configuration register                                                | 0x0024    | varies |
| I2S_TX_CONF1_REG                          | I2S TX configuration register 1                                              | 0x002C    | R/W    |
| I2S_TX_TDM_CTRL_REG                       | I2S TX TDM mode control register                                             | 0x0054    | R/W    |
| **RX timing register**                    |                                                                             |           |        |
| I2S_RX_TIMING_REG                         | I2S RX timing control register                                                | 0x0058    | R/W    |
| **TX timing register**                    |                                                                             |           |        |
| I2S_TX_TIMING_REG                         | I2S TX timing control register                                                | 0x005C    | R/W    |
| **Control and configuration registers**    |                                                                             |           |        |
| I2S_LC_HUNG_CONF_REG                      | I2S timeout configuration register                                           | 0x0060    | R/W    |
| I2S_CONF_SINGLE_DATA_REG                  | I2S single data register                                                     | 0x0068    | R/W    |
| **TX status register**                    |                                                                             |           |        |
| I2S_STATE_REG                             | I2S TX status register                                                        | 0x006C    | RO     |
| **ETM register**                          |                                                                             |           |        |
| I2S_ETM_CONF_REG                          | I2S ETM configure register                                                     | 0x0070    | R/W    |
| **Version register**                      |                                                                             |           |        |
| I2S_DATE_REG                              | Version control register                                                       | 0x0080    | R/W    |
```