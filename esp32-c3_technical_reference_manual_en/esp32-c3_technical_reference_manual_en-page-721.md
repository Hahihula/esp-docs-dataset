

```markdown
Register 28.22. I2C_INT_RAW_REG (0x0020)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                 | (reserved)                                                                  |
| 30  |                                 | Reset                                                                       |
| 29  | I2C_GENERAL_CALL_INT_RAW       | The raw interrupt bit for the I2C_GENERAL_CALL_INT.                         |
| 28  | I2C_SLAVE_STREACH_INT_RAW      | The raw interrupt bit for the I2C_SLAVE_STREACH_INT.                        |
| 27  | I2C_DET_START_INT_RAW          | The raw interrupt bit for the I2C_DET_START_INT.                            |
| 26  | I2C_SCL_MAIN_INT_RAW           | The raw interrupt bit for the I2C_SCL_MAIN_INT.                             |
| 25  | I2C_SCL_ST意图_INT_RAW         | The raw interrupt bit for the I2C_SCL_ST意图_INT.                           |
| 24  | I2C_RXFIFO_UF_INT_RAW          | The raw interrupt bit for the I2C_RXFIFO_UF_INT.                            |
| 23  | I2C_TXFIFO_OVF_INT_RAW         | The raw interrupt bit for the I2C_TXFIFO_OVF_INT.                           |
| 22  | I2C_NACK_TRAN_INT_RAW          | The raw interrupt bit for the I2C_NACK_TRAN_INT.                            |
| 21  | I2C_TRANS_START_INT_RAW        | The raw interrupt bit for the I2C_TRANS_START_INT.                          |
| 20  | I2C_MST_TXFIFO_COMPLETE_INT_RAW| The raw interrupt bit for the I2C_MST_TXFIFO_COMPLETE_INT.                  |
| 19  | I2C_BYTE_TRAN_DONE_INT_RAW     | The raw interrupt bit for the I2C_BYTE_TRAN_DONE_INT.                       |
| 18  | I2C_END_DETECT_INT_RAW         | The raw interrupt bit for the I2C_END_DETECT_INT.                           |
| 17  | I2C_ARBITRATION_LOST_INT_RAW   | The raw interrupt bit for the I2C_ARBITRATION_LOST_INT.                     |
| 16  | I2C_MST_TXFIFO_UDF_INT_RAW     | The raw interrupt bit for the I2C_MST_TXFIFO_UDF_INT.                       |
| 15  | I2C_TXFIFO_WM_INT_RAW          | The raw interrupt bit for the I2C_TXFIFO_WM_INT.                            |
| 14  | I2C_RXFIFO_WM_INT_RAW          | The raw interrupt bit for the I2C_RXFIFO_WM_INT.                            |
| 13  | I2C_RXFIFO_OVF_INT_RAW         | The raw interrupt bit for the I2C_RXFIFO_OVF_INT.                           |
| 12  | I2C_END_DETECT_INT_RAW         | The raw interrupt bit for the I2C_END_DETECT_INT.                           |
| 11  | I2C_ARBITRATION_LOST_INT_RAW   | The raw interrupt bit for the I2C_ARBITRATION_LOST_INT.                     |
| 10  | I2C_MST_TXFIFO_UDF_INT_RAW     | The raw interrupt bit for the I2C_MST_TXFIFO_UDF_INT.                       |
| 9   | I2C_TXFIFO_WM_INT_RAW          | The raw interrupt bit for the I2C_TXFIFO_WM_INT.                            |
| 8   | I2C_RXFIFO_WM_INT_RAW          | The raw interrupt bit for the I2C_RXFIFO_WM_INT.                            |
| 7   | I2C_NACK_TRAN_INT_RAW          | The raw interrupt bit for the I2C_NACK_TRAN_INT.                            |
| 6   | I2C_TRANS_START_INT_RAW        | The raw interrupt bit for the I2C_TRANS_START_INT.                          |
| 5   | I2C_MST_TXFIFO_COMPLETE_INT_RAW| The raw interrupt bit for the I2C_MST_TXFIFO_COMPLETE_INT.                  |
| 4   | I2C_BYTE_TRAN_DONE_INT_RAW     | The raw interrupt bit for the I2C_BYTE_TRAN_DONE_INT.                       |
| 3   | I2C_END_DETECT_INT_RAW         | The raw interrupt bit for the I2C_END_DETECT_INT.                           |
| 2   | I2C_ARBITRATION_LOST_INT_RAW   | The raw interrupt bit for the I2C_ARBITRATION_LOST_INT.                     |
| 1   | I2C_MST_TXFIFO_UDF_INT_RAW     | The raw interrupt bit for the I2C_MST_TXFIFO_UDF_INT.                       |
| 0   |                                 | Reset                                                                       |

I2C_RXFIFO_WM_INT_RAW  The raw interrupt bit for the I2C_RXFIFO_WM_INT interrupt. (R/SS/WTC)

I2C_TXFIFO_WM_INT_RAW  The raw interrupt bit for the I2C_TXFIFO_WM_INT interrupt. (R/SS/WTC)

I2C_RXFIFO_OVF_INT_RAW The raw interrupt bit for the I2C_RXFIFO_OVF_INT interrupt. (R/SS/WTC)

I2C_END_DETECT_INT_RAW The raw interrupt bit for the I2C_END_DETECT_INT interrupt. (R/SS/WTC)

I2C_BYTE_TRAN_DONE_INT_RAW The raw interrupt bit for the I2C_BYTE_TRAN_DONE_INT interrupt. (R/SS/WTC)

I2C_ARBITRATION_LOST_INT_RAW The raw interrupt bit for the I2C_ARBITRATION_LOST_INT interrupt. (R/SS/WTC)

I2C_MST_TXFIFO_UDF_INT_RAW The raw interrupt bit for the I2C_MST_TXFIFO_UDF_INT interrupt. (R/SS/WTC)

I2C_TRANS_COMPLETE_INT_RAW The raw interrupt bit for the I2C_TRANS_COMPLETE_INT interrupt. (R/SS/WTC)

I2C_TIME_OUT_INT_RAW    The raw interrupt bit for the I2C_TIME_OUT_INT interrupt. (R/SS/WTC)

I2C_TRANS_START_INT_RAW The raw interrupt bit for the I2C_TRANS_START_INT interrupt. (R/SS/WTC)

I2C_NACK_INT_RAW         The raw interrupt bit for the I2C_NACK_INT interrupt. (R/SS/WTC)

I2C_TXFIFO_OVF_INT_RAW   The raw interrupt bit for the I2C_TXFIFO_OVF_INT interrupt. (R/SS/WTC)

I2C_RXFIFO_UDF_INT_RAW   The raw interrupt bit for the I2C_RXFIFO_UDF_INT interrupt. (R/SS/WTC)

Continued on the next page...
```