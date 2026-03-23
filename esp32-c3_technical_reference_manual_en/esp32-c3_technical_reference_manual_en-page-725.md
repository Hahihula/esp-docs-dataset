
```markdown
Register 28.25. I2C_INT_STATUS_REG (0x002C)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | RESERVED                                                                     |
| 30  | I2C_GENERAL_CALL_INT_ST                                                     |
| 29  | I2C_SLAVE_STRETCH_INT_ST                                                   |
| 28  | I2C_DET_START_INT_ST                                                        |
| 27  | I2C_SCL_MAIN_TO_INT_ST                                                      |
| 26  | I2C_SDA_MAIN_TO_INT_ST                                                      |
| 25  | I2C_RXFIFO_OVF_INT_ST                                                       |
| 24  | I2C_NACK_INT_ST                                                              |
| 23  | I2C_TRANS_START_INT_ST                                                      |
| 22  | I2C_MST_TXFIFO_UDE_INT_ST                                                   |
| 21  | I2C_BYTE_END_DETECT_INT_ST                                                  |
| 20  | I2C_BYTE_TRAN_DONE_INT_ST                                                   |
| 19  | I2C_ARBITRATION_LOST_INT_ST                                                 |
| 18  | I2C_MST_TXFIFO_UDF_INT_ST                                                   |
| 17  | I2C_TRANS_COMPLETE_INT_ST                                                   |
| 16  | I2C_TIME_OUT_INT_ST                                                          |
| 15  | I2C_RXFIFO_OVF_INT_ST                                                        |
| 14  | I2C_END_DETECT_INT_ST                                                        |
| 13  | I2C_BYTE_TRAN_DONE_INT_ST                                                   |
| 12  | I2C_ARBITRATION_LOST_INT_ST                                                  |
| 11  | I2C_MST_TXFIFO_UDF_INT_ST                                                   |
| 10  | I2C_TRANS_COMPLETE_INT_ST                                                   |
| 9   | I2C_TIME_OUT_INT_ST                                                          |
| 8   | I2C_RXFIFO_OVF_INT_ST                                                        |
| 7   | I2C_END_DETECT_INT_ST                                                         |
| 6   | I2C_BYTE_TRAN_DONE_INT_ST                                                    |
| 5   | I2C_ARBITRATION_LOST_INT_ST                                                  |
| 4   | I2C_MST_TXFIFO_UDF_INT_ST                                                   |
| 3   | I2C_TRANS_COMPLETE_INT_ST                                                   |
| 2   | I2C_TIME_OUT_INT_ST                                                          |
| 1   | I2C_RXFIFO_OVF_INT_ST                                                         |
| 0   | I2C_END_DETECT_INT_ST                                                         |

I2C_RXFIFO_WM_INT_ST The masked interrupt status bit for the I2C_RXFIFO_WM_INT interrupt. (RO)
I2C_TXFIFO_WM_INT_ST The masked interrupt status bit for the I2C_TXFIFO_WM_INT interrupt. (RO)
I2C_RXFIFO_OVF_INT_ST The masked interrupt status bit for the I2C_RXFIFO_OVF_INT interrupt. (RO)
I2C_END_DETECT_INT_ST The masked interrupt status bit for the I2C_END_DETECT_INT interrupt. (RO)
I2C_BYTE_TRAN_DONE_INT_ST The masked interrupt status bit for the I2C_BYTE_TRAN_DONE_INT interrupt. (RO)
I2C_ARBITRATION_LOST_INT_ST The masked interrupt status bit for the I2C_ARBITRATION_LOST_INT interrupt. (RO)
I2C_MST_TXFIFO_UDF_INT_ST The masked interrupt status bit for the I2C_MST_TXFIFO_UDF_INT interrupt. (RO)
I2C_TRANS_COMPLETE_INT_ST The masked interrupt status bit for the I2C_TRANS_COMPLETE_INT interrupt. (RO)
I2C_TIME_OUT_INT_ST The masked interrupt status bit for the I2C_TIME_OUT_INT interrupt. (RO)
I2C_TRANS_START_INT_ST The masked interrupt status bit for the I2C_TRANS_START_INT interrupt. (RO)
I2C_NACK_INT_ST The masked interrupt status bit for the I2C_NACK_INT interrupt. (RO)
I2C_TXFIFO_OVF_INT_ST The masked interrupt status bit for the I2C_TXFIFO_OVF_INT interrupt. (RO)
I2C_RXFIFO_UDF_INT_ST The masked interrupt status bit for the I2C_RXFIFO_UDF_INT interrupt. (RO)

Continued on the next page...
```