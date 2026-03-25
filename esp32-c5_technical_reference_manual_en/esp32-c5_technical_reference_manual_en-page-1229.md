

```markdown
| Name                                       | Description                                                                                      | Address | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|---------|--------|
| Timing registers                           |                                                                                                  |         |        |
| I2C_SCL_LOW_PERIOD_REG                    | Configures the low level width of the SCL Clock                                                | 0x0000  | R/W    |
| I2C_SDA_HOLD_REG                          | Configures the hold time after a negative SCL edge                                              | 0x0030  | R/W    |
| I2C_SDA_SAMPLE_REG                        | Configures the sample time after a positive SCL edge                                             | 0x0034  | R/W    |
| I2C_SCL_HIGH_PERIOD_REG                   | Configures the high level width of SCL                                                            | 0x0038  | R/W    |
| I2C_SCL_START_HOLD_REG                    | Configures the delay between the SDA and SCL negative edge for a start condition                | 0x0040  | R/W    |
| I2C_SCL_RSTART_SETUP_REG                  | Configures the delay between the positive edge of SCL and the negative edge of SDA               | 0x0044  | R/W    |
| I2C_SCL_STOP_HOLD_REG                     | Configures the delay after the SCL clock edge for a stop condition                               | 0x0048  | R/W    |
| I2C_SCL_STOP_SETUP_REG                    | Configures the delay between the SDA and SCL rising edge for a stop condition Measurement unit: i2c_sclk | 0x004C  | R/W    |
| I2C_SCL_ST_TIME_OUT_REG                   | SCL status time out register                                                                     | 0x0078  | R/W    |
| I2C_SCL_MAIN_ST_TIME_OUT_REG              | SCL main status time out register                                                                | 0x007C  | R/W    |
| Configuration registers                    |                                                                                                  |         |        |
| I2C_CTR_REG                               | Transmission setting                                                                             | 0x0004  | varies |
| I2C_TO_REG                                | Setting time out control for receiving data                                                      | 0x000C  | R/W    |
| I2C_SLAVE_ADDR_REG                        | Local slave address setting                                                                      | 0x0010  | R/W    |
| I2C_FIFO_CONF_REG                         | FIFO configuration register                                                                      | 0x0018  | R/W    |
| I2C_FILTER_CFG_REG                        | SCL and SDA filter configuration register                                                       | 0x0050  | R/W    |
| I2C_SCL_SP_CONF_REG                       | Power configuration register                                                                     | 0x0080  | varies |
| I2C_SCL_STRETCH_CONF_REG                  | Set SCL stretch of I2C slave                                                                      | 0x0084  | varies |
| Status registers                           |                                                                                                  |         |        |
| I2C_SR_REG                                | Describe I2C work status                                                                         | 0x0008  | RO     |
| I2C_FIFO_ST_REG                           | FIFO status register                                                                             | 0x0014  | RO     |
| I2C_DATA_REG                              | Rx FIFO read data                                                                                | 0x001C  | HRO    |
| Interrupt registers                        |                                                                                                  |         |        |
| I2C_INT_RAW_REG                           | Raw interrupt status                                                                             | 0x0020  | R/SS   |
|                                            |                                                WTC                                               |         |        |
| I2C_INT_CLR_REG                           | Interrupt clear bits                                                                             | 0x0024  | WT     |
```