
```markdown
Register 29.23. I2C_INT_ENA_REG (0x0028)

| Bit | Name                                      | Description                                                                 |
|-----|--------------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                            | (reserved)                                                                  |
| 30  |                                            | Reset                                                                       |
| 29  | I2C_RXFIFO_WM_INT_ENA                    | Write 1 to enable I2C_RXFIFO_WM_INT interrupt. (R/W)                       |
| 28  | I2C_TXFIFO_WM_INT_ENA                    | Write 1 to enable I2C_TXFIFO_WM_INT interrupt. (R/W)                       |
| 27  | I2C_RXFIFO_OVF_INT_ENA                   | Write 1 to enable I2C_RXFIFO_OVF_INT interrupt. (R/W)                      |
| 26  | I2C_END_DETECT_INT_ENA                   | Write 1 to enable the I2C_END_DETECT_INT interrupt. (R/W)                  |
| 25  | I2C_BYTE_TRANS_DONE_INT_ENA              | Write 1 to enable the I2C_BYTE_TRANS_DONE_INT interrupt. (R/W)             |
| 24  | I2C_ARBITRATION_LOST_INT_ENA             | Write 1 to enable the I2C_ARBITRATION_LOST_INT interrupt. (R/W)            |
| 23  | I2C_MST_TXFIFO_UDF_INT_ENA               | Write 1 to enable I2C_MST_TXFIFO_UDF_INT interrupt. (R/W)                  |
| 22  | I2C_TRANS_COMPLETE_INT_ENA               | Write 1 to enable the I2C_TRANS_COMPLETE_INT interrupt. (R/W)              |
| 21  | I2C_TIME_OUT_INT_ENA                     | Write 1 to enable the I2C_TIME_OUT_INT interrupt. (R/W)                    |
| 20  | I2C_TRANS_START_INT_ENA                  | Write 1 to enable the I2C_TRANS_START_INT interrupt. (R/W)                 |
| 19  | I2C_NACK_INT_ENA                         | Write 1 to enable I2C_NACK_INT interrupt. (R/W)                            |
| 18  | I2C_TXFIFO_OVF_INT_ENA                   | Write 1 to enable I2C_TXFIFO_OVF_INT interrupt. (R/W)                      |
| 17  | I2C_RXFIFO_UDF_INT_ENA                   | Write 1 to enable I2C_RXFIFO_UDF_INT interrupt. (R/W)                      |
| 16  | I2C_SCL_ST_TO_INT_ENA                    | Write 1 to enable I2C_SCL_ST_TO_INT interrupt. (R/W)                       |
| 15  | I2C_SCL_MAIN_ST_TO_INT_ENA               | Write 1 to enable I2C_SCL_MAIN_ST_TO_INT interrupt. (R/W)                  |
| 14  | I2C_DET_START_INT_ENA                    | Write 1 to enable I2C_DET_START_INT interrupt. (R/W)                       |
| 13  | I2C_SLAVE_STRETCH_INT_ENA                | Write 1 to enable I2C_SLAVE_STRETCH_INT interrupt. (R/W)                   |
| 12  | I2C_GENERAL_CALL_INT_ENA                 | Write 1 to enable I2C_GENERAL_CALL_INT interrupt. (R/W)                    |
| 11  | I2C_SLAVE_ADDR_UNMATCH_INT_ENA           | Write 1 to enable I2C_SLAVE_ADDR_UNMATCH_INT interrupt. (R/W)             |
```