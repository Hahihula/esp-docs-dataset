

```markdown
Register 34.24. I2C_INT_STATUS_REG (0x002C)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                    |                                                                             |
| 30  | I2C_SLAVE_ADDR_UNMATCH_INT_ST | The masked interrupt status of I2C_SLAVE_ADDR_UNMATCH_INT. (RO)              |
| 29  | I2C_GENERAL_CALL_INT_ST       | The masked interrupt status of I2C_GENERAL_CALL_INT.                        |
| 28  | I2C_SLAVE_STRETOL_INT_ST      | The masked interrupt status of I2C_SLAVE_STRETOL_INT.                       |
| 27  | I2C_DET_START_INT_ST          | The masked interrupt status of I2C_DET_START_INT.                           |
| 26  | I2C_SCL_MAIN_INT_ST           | The masked interrupt status of I2C_SCL_MAIN_INT.                            |
| 25  | I2C_SCL_STO_INT_ST            | The masked interrupt status of I2C_SCL_STO_INT.                             |
| 24  | I2C_RXFIFO_OVF_INT_ST         | The masked interrupt status of I2C_RXFIFO_OVF_INT.                          |
| 23  | I2C_TXFIFO_UDF_INT_ST         | The masked interrupt status of I2C_TXFIFO_UDF_INT.                          |
| 22  | I2C_NACK_INT_ST               | The masked interrupt status of I2C_NACK_INT.                                |
| 21  | I2C_TRAN_TIME_OUT_INT_ST      | The masked interrupt status of I2C_TRAN_TIME_OUT_INT.                       |
| 20  | I2C_MST_TXFIFO_COMPLETE_INT_ST| The masked interrupt status of I2C_MST_TXFIFO_COMPLETE_INT.                  |
| 19  | I2C_BYTE_TRANS_DONE_INT_ST    | The masked interrupt status of I2C_BYTE_TRANS_DONE_INT. (RO)                 |
| 18  | I2C_ARBITRATION_LOST_INT_ST   | The masked interrupt status of I2C_ARBITRATION_LOST_INT. (RO)                |
| 17  | I2C_MST_TXFIFO_UDF_INT_ST     | The masked interrupt status of I2C_MST_TXFIFO_UDF_INT.                       |
| 16  | I2C_TRAN_COMPLETE_INT_ST      | The masked interrupt status of I2C_TRAN_COMPLETE_INT. (RO)                   |
| 15  | I2C_TIME_OUT_INT_ST           | The masked interrupt status of I2C_TIME_OUT_INT. (RO)                        |
| 14  | I2C_TRAN_START_INT_ST         | The masked interrupt status of I2C_TRAN_START_INT. (RO)                      |
| 13  | I2C_NACK_INT_ST               | The masked interrupt status of I2C_NACK_INT. (RO)                            |
| 12  | I2C_TXFIFO_OVF_INT_ST         | The masked interrupt status of I2C_TXFIFO_OVF_INT. (RO)                      |

I2C_RXFIFO_WM_INT_ST   The masked interrupt status of I2C_RXFIFO_WM_INT interrupt. (RO)
I2C_TXFIFO_WM_INT_ST   The masked interrupt status of I2C_TXFIFO_WM_INT interrupt. (RO)
I2C_RXFIFO_OVF_INT_ST  The masked interrupt status of I2C_RXFIFO_OVF_INT interrupt. (RO)
I2C_END_DETECT_INT_ST  The masked interrupt status of the I2C_END_DETECT_INT interrupt. (RO)
I2C_BYTE_TRANS_DONE_INT_ST   The masked interrupt status of the I2C_BYTE_TRANS_DONE_INT interrupt. (RO)
I2C_ARBITRATION_LOST_INT_ST  The masked interrupt status of the I2C_ARBITRATION_LOST_INT interrupt. (RO)
I2C_MST_TXFIFO_UDF_INT_ST   The masked interrupt status of I2C_MST_TXFIFO_UDF_INT interrupt. (RO)
I2C_TRAN_COMPLETE_INT_ST    The masked interrupt status of the I2C_TRAN_COMPLETE_INT interrupt. (RO)
I2C_TIME_OUT_INT_ST         The masked interrupt status of the I2C_TIME_OUT_INT interrupt. (RO)
I2C_TRAN_START_INT_ST       The masked interrupt status of the I2C_TRAN_START_INT interrupt. (RO)
I2C_NACK_INT_ST             The masked interrupt status of I2C_NACK_INT interrupt. (RO)
I2C_TXFIFO_OVF_INT_ST       The masked interrupt status of I2C_TXFIFO_OVF_INT interrupt. (RO)

Continued on the next page...
```