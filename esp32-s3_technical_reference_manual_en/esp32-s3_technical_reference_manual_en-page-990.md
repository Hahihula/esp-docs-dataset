**Title: Chapter 27 I2C Controller (I2C)**

**Table Title: Table 27-4-1. I2C Synchronous Registers**

| Register                   | Parameter                                    | Address |
|----------------------------|----------------------------------------------|---------|
| **I2C_CTR_REG**            |                                              |         |
|                            | I2C_SLV_TX_AUTO_START_EN                    | 0x0004  |
|                            | I2C_ADDR_10BIT_RW_CHECK_EN                  |         |
|                            | I2C_ADDR_BROADCASTING_EN                     |         |
|                            | I2C_SDA FORCE OUT                             |         |
|                            | I2C_SCL FORCE OUT                             |         |
|                            | I2C_SAMPLE_SCL_LEVEL                          |         |
|                            | I2C_RX_FULL_ACK_LEVEL                        |         |
|                            | I2C_MS_MODE                                  |         |
|                            | I2C_TX_LSB_FIRST                              |         |
|                            | I2C_RX_LSB_FIRST                              |         |
|                            | I2C_ARBITRATION_EN                           |         |
| **I2C_TO_REG**             |                                              | 0x000C  |
|                            | I2C_TIME_OUT_EN                              |         |
|                            | I2C_TIME_OUT_VALUE                           |         |
|                            | I2C_SLAVE_ADDR_REG                           | 0x0010  |
|                            | I2C_SLAVE_ADDR                               |         |
| **I2C_FIFO_CONF_REG**      |                                              | 0x0018  |
|                            | I2C_FIFO_ADDR_CFG_EN                         |         |
| **I2C_SCL_SP_CONF_REG**    |                                              | 0x0080  |
|                            | I2C_SDA_PD_EN                                |         |
|                            | I2C_SCL_PD_EN                                |         |
|                            | I2C_SCL_RST_SLV_NUM                          |         |
| **I2C_SCL_STRETCH_CONF_REG** |                                              | 0x0084  |
|                            | I2C_SCL_BYTE_ACK_CTL_EN                      |         |
|                            | I2C_SLAVE_BYTE_ACK_LVL                       |         |
|                            | I2C_SDA_STRETCH_EN                           |         |
| **I2C_SCL_LOW_PERIOD_REG** |                                              | 0x0000  |
|                            | I2C_SCL_LOW_PERIOD_EN                        |         |
| **I2C_SCL_HIGH_PERIOD_REG** |                                              | 0x0038  |
|                            | I2C_WAIT_HIGH_PERIOD                          |         |
| **I2C_SDA_HOLD_REG**        |                                              | 0x0030  |
|                            | I2C_SDA_HOLD_TIME                             |         |
| **I2C_SDA_SAMPLE_REG**      |                                              | 0x0034  |
|                            | I2C_SDA_SAMPLE_TIME                           |         |
| **I2C_SCL_START_HOLD_REG** |                                              | 0x0040  |
|                            | I2C_SCL_START_HOLD_TIME                       |         |
| **I2C_SCL_RSTART_SETUP_REG** |                                             | 0x0044  |
|                            | I2C_SCL_RST_START_TIME                        |         |
| **I2C_SCL_STOP_HOLD_REG**   |                                              | 0x0048  |
|                            | I2C_SCL_STOP_HOLD_TIME                        |         |
| **I2C_SCL_STOP_SETUP_REG**  |                                              | 0x004C  |
|                            | I2C_SCL_STOP_SETUP_TIME                       |         |
| **I2C_SCL_ST_TIME_OUT_REG** |                                             | 0x0078  |
|                            | I2C_SCL_ST_TO_I2C                             |         |
| **I2C_SCL_MAIN_ST_TIME_OUT_REG** |                                          | 0x007C  |
|                            | I2C_SCLMain_ST_TO_I2C                         |         |
| **I2C_FILTER_CFG_REG**      |                                              | 0x0050  |
|                            | I2C_SCL_FILTER_EN                             |         |
|                            | I2C_SCL_FILTER_THRES                          |         |
|                            | I2C_SDA_FILTER_EN                             |         |
|                            | I2C_SDA_FILTER_THRES                         |         |

**Section Title: **

**Subtitle:** Open-Drain Output  
**Body Text:** SCL and SDA output drivers must be configured as open drain. There are two ways to achieve this:

**Footer Information:**  
Espressif Systems  
990  
Submit Documentation Feedback  

**Document Reference:** ESP32-S3 TRM (Version 1.7)