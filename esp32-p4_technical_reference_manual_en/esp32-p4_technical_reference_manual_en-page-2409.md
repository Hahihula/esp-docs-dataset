
Register 44.22. I2C_INT_CLR_REG (0x0024)

| Bit | Field Name                                 |
|-----|--------------------------------------------|
| 31  | (reserved)                                |
| 30  | I2C_SLAVE_ADDR_UNMATCH_INT_CLR            |
| 29  | I2C_GENERAL_CALL_INT_CLR                  |
| 28  | I2C_SCL_ST_TO_INT_CLR                     |
| 27  | I2C_SDA_DET_START_INT_CLR                 |
| 26  | I2C_SLAVE_STRETCH_INT_CLR                 |
| 25  | I2C_SCL_MAIN_ST_TO_INT_CLR                |
| 24  | I2C_TXFIFO_OVF_INT_CLR                    |
| 23  | I2C_RXFIFO_WM_INT_CLR                     |
| 22  | I2C_NACK_INT_CLR                          |
| 21  | I2C_MST_TXFIFO_UDF_INT_CLR                |
| 20  | I2C_TRANS_COMPLETE_INT_CLR                |
| 19  | I2C_TIME_OUT_INT_CLR                      |
| 18  | I2C_TRANS_START_INT_CLR                   |
| 17  | I2C_BYTE_TRAN_DONE_INT_CLR                |
| 16  | I2C_END_DETECT_INT_CLR                    |
| 15  | I2C_RXFIFO_OVF_INT_CLR                    |
| 14  | I2C_ARBITRATION_LOST_INT_CLR              |
| 13  | (reserved)                                |
| 12  | I2C_RXFIFO_WM_INT_CLR                     |
| 11  | I2C_TXFIFO_WM_INT_CLR                     |
| 10  | I2C_NACK_INT_CLR                          |
| 9   | I2C_MST_TXFIFO_UDF_INT_CLR                |
| 8   | I2C_TRANS_COMPLETE_INT_CLR                |
| 7   | I2C_TIME_OUT_INT_CLR                      |
| 6   | I2C_TRANS_START_INT_CLR                   |
| 5   | I2C_BYTE_TRAN_DONE_INT_CLR                |
| 4   | I2C_END_DETECT_INT_CLR                    |
| 3   | I2C_RXFIFO_OVF_INT_CLR                    |
| 2   | I2C_ARBITRATION_LOST_INT_CLR              |
| 1   | (reserved)                                |
| 0   | Reset                                     |

I2C_RXFIFO_WM_INT_CLR Write 1 to clear I2C_RXFIFO_WM_INT interrupt. (WT)

I2C_TXFIFO_WM_INT_CLR Write 1 to clear I2C_TXFIFO_WM_INT interrupt. (WT)

I2C_RXFIFO_OVF_INT_CLR Write 1 to clear I2C_RXFIFO_OVF_INT interrupt. (WT)

I2C_END_DETECT_INT_CLR Write 1 to clear the I2C_END_DETECT_INT interrupt. (WT)

I2C_BYTE_TRAN_DONE_INT_CLR Write 1 to clear the I2C_BYTE_TRAN_DONE_INT interrupt. (WT)

I2C_ARBITRATION_LOST_INT_CLR Write 1 to clear the I2C_ARBITRATION_LOST_INT interrupt. (WT)

I2C_MST_TXFIFO_UDF_INT_CLR Write 1 to clear I2C_MST_TXFIFO_UDF_INT interrupt. (WT)

I2C_TRANS_COMPLETE_INT_CLR Write 1 to clear the I2C_TRANS_COMPLETE_INT interrupt. (WT)

I2C_TIME_OUT_INT_CLR Write 1 to clear the I2C_TIME_OUT_INT interrupt. (WT)

I2C_TRANS_START_INT_CLR Write 1 to clear the I2C_TRANS_START_INT interrupt. (WT)

I2C_NACK_INT_CLR Write 1 to clear I2C_NACK_INT interrupt. (WT)

I2C_TXFIFO_OVF_INT_CLR Write 1 to clear I2C_TXFIFO_OVF_INT interrupt. (WT)

I2C_RXFIFO_UDF_INT_CLR Write 1 to clear I2C_RXFIFO_UDF_INT interrupt. (WT)

I2C_SCL_ST_TO_INT_CLR Write 1 to clear I2C_SCL_ST_TO_INT interrupt. (WT)

I2C_SCL_MAIN_ST_TO_INT_CLR Write 1 to clear I2C_SCL_MAIN_ST_TO_INT interrupt. (WT)

I2C_DET_START_INT_CLR Write 1 to clear I2C_DET_START_INT interrupt. (WT)

I2C_SLAVE_STRETCH_INT_CLR Write 1 to clear I2C_SLAVE_STRETCH_INT interrupt. (WT)

I2C_GENERAL_CALL_INT_CLR Write 1 to clear I2C_GENARAL_CALL_INT interrupt. (WT)

I2C_SLAVE_ADDR_UNMATCH_INT_CLR Write 1 to clear I2C_SLAVE_ADDR_UNMATCH_INT_RAW interrupt. (WT)