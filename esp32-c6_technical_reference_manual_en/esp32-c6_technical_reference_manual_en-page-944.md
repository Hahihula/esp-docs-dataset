

```markdown
Register 29.22. I2C_INT_CLR_REG (0x0024)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | I2C_SLAVE_ADDR_UNMATCH_INT_CLR             | Write 1 to clear I2C_SLAVE_ADDR_UNMATCH_INT interrupt. (WT)                 |
| 29  | I2C_GENERAL_CALL_INT_CLR                   | Write 1 to clear I2C_GENERAL_CALL_INT interrupt. (WT)                       |
| 28  | I2C_SCL_ST_TO_INT_CLR                      | Write 1 to clear I2C_SCL_ST_TO_INT interrupt. (WT)                          |
| 27  | I2C_SDA_DET_START_INT_CLR                  | Write 1 to clear I2C_SDA_DET_START_INT interrupt. (WT)                      |
| 26  | I2C_SLAVE_STRETCH_INT_CLR                  | Write 1 to clear I2C_SLAVE_STRETCH_INT interrupt. (WT)                      |
| 25  | I2C_SCL_MAIN_ST_TO_INT_CLR                 | Write 1 to clear I2C_SCL_MAIN_ST_TO_INT interrupt. (WT)                     |
| 24  | I2C_TXFIFO_OVF_INT_CLR                     | Write 1 to clear I2C_TXFIFO_OVF_INT interrupt. (WT)                         |
| 23  | I2C_RXFIFO_UVF_INT_CLR                     | Write 1 to clear I2C_RXFIFO_UVF_INT interrupt. (WT)                         |
| 22  | I2C_NACK_INT_CLR                           | Write 1 to clear I2C_NACK_INT interrupt. (WT)                               |
| 21  | I2C_TRANS_START_INT_CLR                    | Write 1 to clear the I2C_TRANS_START_INT interrupt. (WT)                    |
| 20  | I2C_TIME_OUT_INT_CLR                       | Write 1 to clear the I2C_TIME_OUT_INT interrupt. (WT)                       |
| 19  | I2C_TRANS_COMPLETE_INT_CLR                 | Write 1 to clear the I2C_TRANS_COMPLETE_INT interrupt. (WT)                 |
| 18  | I2C_MST_TXFIFO_UDF_INT_CLR                 | Write 1 to clear I2C_MST_TXFIFO_UDF_INT interrupt. (WT)                     |
| 17  | I2C_END_DETECT_INT_CLR                     | Write 1 to clear the I2C_END_DETECT_INT interrupt. (WT)                     |
| 16  | I2C_RXFIFO_OVF_INT_CLR                     | Write 1 to clear I2C_RXFIFO_OVF_INT interrupt. (WT)                         |
| 15  | I2C_BYTE_TRANS_DONE_INT_CLR                | Write 1 to clear the I2C_BYTE_TRANS_DONE_INT interrupt. (WT)                |
| 14  | I2C_ARBITRATION_LOST_INT_CLR               | Write 1 to clear the I2C_ARBITRATION_LOST_INT interrupt. (WT)               |
| 13  | I2C_TXFIFO_WM_INT_CLR                      | Write 1 to clear I2C_TXFIFO_WM_INT interrupt. (WT)                          |
| 12  | I2C_RXFIFO_WM_INT_CLR                      | Write 1 to clear I2C_RXFIFO_WM_INT interrupt. (WT)                          |
```