
```markdown
Register 29.24. I2C_INT_STATUS_REG (0x002C)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                 | (reserved)                                                                  |
| 19  | I2C_SLAVE_ADDR_UNMATCH_INT_ST   | The masked interrupt status of the I2C_SLAVE_ADDR_UNMATCH_INT interrupt.    |
| 18  | I2C_GENERAL_CALL_INT_ST         | The masked interrupt status of the I2C_GENERAL_CALL_INT interrupt.          |
| 17  | I2C_SLAVE_STRETOL_INT_ST        | The masked interrupt status of the I2C_SLAVE_STRETOL_INT interrupt.         |
| 16  | I2C_DET_START_INT_ST            | The masked interrupt status of the I2C_DET_START_INT interrupt.             |
| 15  | I2C_SCL_MAIN_INT_ST             | The masked interrupt status of the I2C_SCL_MAIN_INT interrupt.              |
| 14  | I2C_SCL_ST_INT_ST               | The masked interrupt status of the I2C_SCL_ST_INT interrupt.                |
| 13  | I2C_RXFIFO_OVF_INT_ST           | The masked interrupt status of the I2C_RXFIFO_OVF_INT interrupt.            |
| 12  | I2C_NACK_INT_ST                 | The masked interrupt status of the I2C_NACK_INT interrupt.                  |
| 11  | I2C_TRANS_OUT_INT_ST            | The masked interrupt status of the I2C_TRANS_OUT_INT interrupt.             |
| 10  | I2C_MST_TXFIFO_UDF_INT_ST       | The masked interrupt status of the I2C_MST_TXFIFO_UDF_INT interrupt.        |
| 9   | I2C_BYTE_TRAN_COMPLETE_INT_ST   | The masked interrupt status of the I2C_BYTE_TRAN_COMPLETE_INT interrupt.    |
| 8   | I2C_RXFIFO_WWM_INT_ST           | The masked interrupt status of the I2C_RXFIFO_WWM_INT interrupt.            |
| 7   |                                 |                                                                             |
| 6   |                                 |                                                                             |
| 5   |                                 |                                                                             |
| 4   |                                 |                                                                             |
| 3   |                                 |                                                                             |
| 2   |                                 |                                                                             |
| 1   |                                 |                                                                             |
| 0   |                                 | Reset                                                                        |

I2C_RXFIFO_WWM_INT_ST The masked interrupt status status of I2C_RXFIFO_WWM_INT interrupt. (RO)
I2C_TXFIFO_WWM_INT_ST The masked interrupt status status of I2C_TXFIFO_WWM_INT interrupt. (RO)
I2C_RXFIFO_OVF_INT_ST The masked interrupt status status of I2C_RXFIFO_OVF_INT interrupt. (RO)
I2C_END_DETECT_INT_ST The masked interrupt status status of the I2C_END_DETECT_INT interrupt. (RO)
I2C_BYTE_TRAN_DONE_INT_ST The masked interrupt status status of the I2C_BYTE_TRAN_DONE_INT interrupt. (RO)
I2C_ARBITRATION_LOST_INT_ST The masked interrupt status status of the I2C_ARBITRATION_LOST_INT interrupt. (RO)
I2C_MST_TXFIFO_UDF_INT_ST The masked interrupt status status of I2C_MST_TXFIFO_UDF_INT interrupt. (RO)
I2C_TRANS_COMPLETE_INT_ST The masked interrupt status status of the I2C_TRANS_COMPLETE_INT interrupt. (RO)
I2C_TIME_OUT_INT_ST The masked interrupt status status of the I2C_TIME_OUT_INT interrupt. (RO)
I2C_TRANS_START_INT_ST The masked interrupt status status of the I2C_TRANS_START_INT interrupt. (RO)
I2C_NACK_INT_ST The masked interrupt status status of I2C_NACK_INT interrupt. (RO)
I2C_TXFIFO_OVF_INT_ST The masked interrupt status status of I2C_TXFIFO_OVF_INT interrupt. (RO)

Continued on the next page...
```