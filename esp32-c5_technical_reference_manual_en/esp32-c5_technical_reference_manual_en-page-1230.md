

```markdown
| Name                        | Description                  | Address   | Access |
|-----------------------------|------------------------------|-----------|--------|
| I2C_INT_ENA_REG             | Interrupt enable bits        | 0x0028    | R/W    |
| I2C_INT_STATUS_REG          | Status of captured I2C communication events | 0x002C   | RO     |

**Command registers**

| Name                        | Description                  | Address   | Access |
|-----------------------------|------------------------------|-----------|--------|
| I2C_COMDO_REG               | I2C command register 0       | 0x0058    | varies |
| I2C_COMD1_REG               | I2C command register 1       | 0x005C    | varies |
| I2C_COMD2_REG               | I2C command register 2       | 0x0060    | varies |
| I2C_COMD3_REG               | I2C command register 3       | 0x0064    | varies |
| I2C_COMD4_REG               | I2C command register 4       | 0x0068    | varies |
| I2C_COMD5_REG               | I2C command register 5       | 0x006C    | varies |
| I2C_COMD6_REG               | I2C command register 6       | 0x0070    | varies |
| I2C_COMD7_REG               | I2C command register 7       | 0x0074    | varies |

**Version register**

| Name                        | Description                  | Address   | Access |
|-----------------------------|------------------------------|-----------|--------|
| I2C_DATE_REG                | Version register             | 0x00F8    | R/W    |

**Address register**

| Name                        | Description                  | Address   | Access |
|-----------------------------|------------------------------|-----------|--------|
| I2C_TXFIFO_START_ADDR_REG   | I2C TX FIFO base address register | 0x0100   | HRO    |
| I2C_RXFIFO_START_ADDR_REG   | I2C RX FIFO base address register | 0x0180   | HRO    |

### 34.8.2 LP_I2C Register Summary

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                        | Description                                                                                      | Address   | Access |
|-----------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| **Timing Registers**                                                        |                                                                                                  |           |        |
| LP_I2C_SCL_LOW_PERIOD_REG    | Configures the low level width of the SCL Clock                                                 | 0x0000    | R/W    |
| LP_I2C_SDA_HOLD_REG          | Configures the hold time after a negative SCL edge                                              | 0x0030    | R/W    |
| LP_I2C_SDA_SAMPLE_REG        | Configures the sample time after a positive SCL edge                                             | 0x0034    | R/W    |
| LP_I2C_SCL_HIGH_PERIOD_REG   | Configures the high level width of SCL                                                           | 0x0038    | R/W    |
| LP_I2C_SCL_START_HOLD_REG    | Configures the delay between the SDA and SCL negative edge for a start condition                 | 0x0040    | R/W    |
| LP_I2C_SCL_RSTART_SETUP_REG  | Configures the delay between the positive edge of SCL and the negative edge of SDA                | 0x0044    | R/W    |
| LP_I2C_SCL_STOP_HOLD_REG     | Configures the delay after the SCL clock edge for a stop condition                               | 0x0048    | R/W    |
| LP_I2C_SCL_STOP_SETUP_REG    | Configures the delay between the SDA and SCL positive edge for a stop condition                  | 0x004C    | R/W    |
| LP_I2C_SCL_ST_TIME_OUT_REG   | SCL status time out register                                                                     | 0x0078    | R/W    |
| LP_I2C_SCL_MAIN_ST_TIME_OUT_REG | SCL main status time out register                                                               | 0x007C    | R/W    |

| **Configuration Registers**                                                |                                                                                                  |           |        |
|-----------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| LP_I2C_CTR_REG              | Transmission setting                                                                             | 0x0004    | varies |
| LP_I2C_TO_REG               | Setting time out control for receiving data                                                      | 0x000C    | R/W    |
| LP_I2C_FIFO_CONF_REG        | FIFO configuration register                                                                      | 0x0018    | R/W    |
| LP_I2C_FILTER_CFG_REG       | SCL and SDA filter configuration register                                                        | 0x0050    | R/W    |
```