

```markdown
Register 44.55. LP_I2C_INT_CLR_REG (0x0024)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | Reset                                                                      |
| 30  |                                | Reserved                                                                   |
| 29  | LP_I2C_DET_START_INT_CLR       | Write 1 to clear LP_I2C_DET_START_INT interrupt. (WT)                       |
| 28  | LP_I2C_SCL_MAIN_ST_TO_INT_CLR  | Write 1 to clear LP_I2C_SCL_MAIN_ST_TO_INT interrupt. (WT)                  |
| 27  | LP_I2C_SCL_ST_TO_INT_CLR       | Write 1 to clear LP_I2C_SCL_ST_TO_INT interrupt. (WT)                       |
| 26  | LP_I2C_RXFIFO_UDF_INT_CLR      | Write 1 to clear LP_I2C_RXFIFO_UDF_INT interrupt. (WT)                      |
| 25  | LP_I2C_TXFIFO_OVF_INT_CLR      | Write 1 to clear LP_I2C_TXFIFO_OVF_INT interrupt. (WT)                      |
| 24  | LP_I2C_NACK_INT_CLR            | Write 1 to clear LP_I2C_SLAVE_STRETCH_INT interrupt. (WT)                  |
| 23  | LP_I2C_TRANS_START_INT_CLR     | Write 1 to clear the LP_I2C_TRANS_START_INT interrupt. (WT)                 |
| 22  | LP_I2C_TIME_OUT_INT_CLR        | Write 1 to clear the LP_I2C_TIME_OUT_INT interrupt. (WT)                    |
| 21  | LP_I2C_TRANS_COMPLETE_INT_CLR  | Write 1 to clear the LP_I2C_TRANS_COMPLETE_INT interrupt. (WT)              |
| 20  | LP_I2C_MST_TXFIFO_UDF_INT_CLR  | Write 1 to clear LP_I2C_MST_TXFIFO_UDF_INT interrupt. (WT)                  |
| 19  | LP_I2C_ARBITRATION_LOST_INT_CLR| Write 1 to clear the LP_I2C_ARBITRATION_LOST_INT interrupt. (WT)            |
| 18  | LP_I2C_END_DETECT_INT_CLR      | Write 1 to clear the LP_I2C_END_DETECT_INT interrupt. (WT)                  |
| 17  | LP_I2C_BYTE_TRANS_DONE_INT_CLR | Write 1 to clear the LP_I2C_BYTE_TRANS_DONE_INT interrupt. (WT)             |
| 16  | LP_I2C_TIME_OUT_INT_CLR        | Write 1 to clear the LP_I2C_TIME_OUT_INT interrupt. (WT)                    |
| 15  | LP_I2C_TXFIFO_OVF_INT_CLR      | Write 1 to clear LP_I2C_TXFIFO_OVF_INT interrupt. (WT)                      |
| 14  | LP_I2C_RXFIFO_WM_INT_CLR       | Write 1 to clear LP_I2C_RXFIFO_WM_INT interrupt. (WT)                       |
| 13  | LP_I2C_TXFIFO_WM_INT_CLR       | Write 1 to clear LP_I2C_TXFIFO_WM_INT interrupt. (WT)                      |
| 12  | LP_I2C_RXFIFO_OVF_INT_CLR      | Write 1 to clear LP_I2C_RXFIFO_OVF_INT interrupt. (WT)                      |
| 11  | LP_I2C_END_DETECT_INT_CLR      | Write 1 to clear the LP_I2C_END_DETECT_INT interrupt. (WT)                  |
| 10  | LP_I2C_BYTE_TRANS_DONE_INT_CLR | Write 1 to clear the LP_I2C_BYTE_TRANS_DONE_INT interrupt. (WT)             |
| 9   | LP_I2C_ARBITRATION_LOST_INT_CLR| Write 1 to clear the LP_I2C_ARBITRATION_LOST_INT interrupt. (WT)            |
| 8   | LP_I2C_MST_TXFIFO_UDF_INT_CLR  | Write 1 to clear LP_I2C_MST_TXFIFO_UDF_INT interrupt. (WT)                  |
| 7   | LP_I2C_SCL_ST_TO_INT_CLR       | Write 1 to clear LP_I2C_SCL_ST_TO_INT interrupt. (WT)                       |
| 6   | LP_I2C_SCL_MAIN_ST_TO_INT_CLR  | Write 1 to clear LP_I2C_SCL_MAIN_ST_TO_INT interrupt. (WT)                  |
| 5   | LP_I2C_NACK_INT_CLR            | Write 1 to clear LP_I2C_SLAVE_STRETCH_INT interrupt. (WT)                   |
| 4   | LP_I2C_TRANS_START_INT_CLR     | Write 1 to clear the LP_I2C_TRANS_START_INT interrupt. (WT)                 |
| 3   | LP_I2C_TIME_OUT_INT_CLR        | Write 1 to clear the LP_I2C_TIME_OUT_INT interrupt. (WT)                    |
| 2   | LP_I2C_TRANS_COMPLETE_INT_CLR  | Write 1 to clear the LP_I2C_TRANS_COMPLETE_INT interrupt. (WT)              |
| 1   | LP_I2C_MST_TXFIFO_UDF_INT_CLR  | Write 1 to clear LP_I2C_MST_TXFIFO_UDF_INT interrupt. (WT)                  |
| 0   | Reset                          |                                                                             |
```