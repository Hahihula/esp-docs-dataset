

```markdown
| Register                     | Field                                                                 | Address |
|------------------------------|------------------------------------------------------------------------|---------|
| I2C_CTR_REG                 | I2C_SLV_TX_AUTO_START_EN<br>I2C_ADDR_10BIT_RW_CHECK_EN<br>I2C_ADDR_BROADCASTING_EN<br>I2C_SDA_FORCE_OUT<br>I2C_SCL_FORCE_OUT<br>I2C_SAMPLE_SCL_LEVEL<br>I2C_RX_FULL_ACK_LEVEL<br>I2C_MS_MODE<br>I2C_TX_LSB_FIRST<br>I2C_RX_LSB_FIRST<br>I2C_ARBITRATION_EN | 0x0004  |
| I2C_TO_REG                  | I2C_TIME_OUT_EN<br>I2C_TIME_OUT_VALUE                                | 0x000C  |
| I2C_SLAVE_ADDR_REG          | I2C_ADDR_10BIT_EN<br>I2C_SLAVE_ADDR                                  | 0x0010  |
| I2C_FIFO_CONF_REG           | I2C_FIFO_ADDR_CFG_EN                                                  | 0x0018  |
| I2C_SCL_SP_CONF_REG         | I2C_SDA_PD_EN<br>I2C_SCL_PD_EN<br>I2C_SCL_RST_SLV_NUM<br>I2C_SCL_RST_SLV_EN | 0x0080  |
| I2C_SCL_STRETCH_CONF_REG    | I2C_SLAVE_BYTE_ACK_CTL_EN<br>I2C_SLAVE_BYTE_ACK_LVL<br>I2C_SLAVE_SCL_STRETCH_EN<br>I2C_STRETCH_PROTECT_NUM | 0x0084  |
| I2C_SCL_LOW_PERIOD_REG      | I2C_SCL_LOW_PERIOD                                                    | 0x0000  |
| I2C_SCL_HIGH_PERIOD_REG     | I2C_WAIT_HIGH_PERIOD                                                  | 0x0038  |
| I2C_SDA_HOLD_REG            | I2C_HIGH_PERIOD                                                        | 0x0030  |
| I2C_SDA_SAMPLE_REG          | I2C_SDA_SAMPLE_TIME                                                   | 0x0034  |
| I2C_SCL_START_HOLD_REG      | I2C_SCL_START_HOLD_TIME                                               | 0x0040  |
| I2C_SCL_RSTART_SETUP_REG     | I2C_SCL_RSTART_SETUP_TIME                                             | 0x0044  |
| I2C_SCL_STOP_HOLD_REG        | I2C_SCL_STOP_HOLD_TIME                                                | 0x0048  |
| I2C_SCL_STOP_SETUP_REG       | I2C_SCL_STOP_SETUP_TIME                                               | 0x004C  |
| I2C_SCL_ST_TIME_OUT_REG      | I2C_SCL_ST_TO_I2C                                                     | 0x0078  |
| I2C_SCL_MAIN_ST_TIME_OUT_REG | I2C_SCL_MAIN_ST_TO_I2C                                                | 0x007C  |
| I2C_FILTER_CFG_REG           | I2C_SCL_FILTER_EN<br>I2C_SCL_FILTER_THRES<br>I2C_SDA_FILTER_EN<br>I2C_SDA_FILTER_THRES | 0x0050  |
```

## 27.4.6 Open-Drain Output

SCL and SDA output drivers must be configured as open-drain. There are two ways to achieve this:
```markdown
Espressif Systems          969            ESP32-C61 TRM (Pre-release v0.5)
Submit Documentation Feedback        PRELIMINARY
```