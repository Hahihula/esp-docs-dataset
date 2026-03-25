
```markdown
Register 27.24. I2C_INT_STATUS_REG (0x002C)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                     |                                                                             |
| 19  | I2C_SLAVE_ADDR_UNMATCH_INT_ST  | The masked interrupt status of the I2C_SLAVE_ADDR_UNMATCH_INT.              |
| 18  | I2C_GENERAL_CALL_INT_ST        | The masked interrupt status of the I2C_GENERAL_CALL_INT.                    |
| 17  | I2C_SLAVE_STRETCH_INT_ST       | The masked interrupt status of the I2C_SLAVE_STRETCH_INT.                   |
| 16  | I2C_DET_START_INT_ST           | The masked interrupt status of the I2C_DET_START_INT.                       |
| 15  | I2C_SCL_MAIN_INT_ST            | The masked interrupt status of the I2C_SCL_MAIN_INT.                        |
| 14  | I2C_SCL_STO_INT_ST             | The masked interrupt status of the I2C_SCL_STO_INT.                         |
| 13  | I2C_RXFIFO_OVF_INT_ST          | The masked interrupt status of the I2C_RXFIFO_OVF_INT.                      |
| 12  | I2C_NACK_INT_ST                | The masked interrupt status of the I2C_NACK_INT.                            |
| 11  | I2C_TRAN_INT_ST                | The masked interrupt status of the I2C_TRAN_INT.                            |
| 10  | I2C_TIME_OUT_INT_ST            | The masked interrupt status of the I2C_TIME_OUT_INT.                        |
| 9   | I2C_MST_TXFIFO_UDE_INT_ST      | The masked interrupt status of the I2C_MST_TXFIFO_UDE_INT.                  |
| 8   | I2C_BYTE_TRAN_COMPLETE_INT_ST  | The masked interrupt status of the I2C_BYTE_TRAN_COMPLETE_INT.              |
| 7   | I2C_END_DETECT_INT_ST          | The masked interrupt status of the I2C_END_DETECT_INT.                      |
| 6   | I2C_ARBITRATION_LOST_INT_ST    | The masked interrupt status of the I2C_ARBITRATION_LOST_INT.                |
| 5   | I2C_MST_TXFIFO_UDF_INT_ST      | The masked interrupt status of the I2C_MST_TXFIFO_UDF_INT.                  |
| 4   | I2C_TRAN_COMPLETE_INT_ST       | The masked interrupt status of the I2C_TRAN_COMPLETE_INT.                   |
| 3   | I2C_TIME_OUT_INT_ST            | The masked interrupt status of the I2C_TIME_OUT_INT.                        |
| 2   | I2C_TRAN_START_INT_ST          | The masked interrupt status of the I2C_TRAN_START_INT.                      |
| 1   | I2C_NACK_INT_ST                | The masked interrupt status of the I2C_SLAVE_STRETCH_INT.                   |
| 0   | I2C_TXFIFO_OVF_INT_ST          | The masked interrupt status of the I2C_TXFIFO_OVF_INT.                      |

I2C_RXFIFO_WM_INT_ST (RO)    The masked interrupt status status of I2C_RXFIFO_WM_INT interrupt.
I2C_TXFIFO_WM_INT_ST (RO)    The masked interrupt status status of I2C_TXFIFO_WM_INT interrupt.
I2C_RXFIFO_OVF_INT_ST (RO)   The masked interrupt status status of I2C_RXFIFO_OVF_INT interrupt.
I2C_END_DETECT_INT_ST (RO)   The masked interrupt status status of the I2C_END_DETECT_INT interrupt.
I2C_BYTE_TRAN_DONE_INT_ST (RO) The masked interrupt status status of the I2C_END_DETECT_INT interrupt.
I2C_ARBITRATION_LOST_INT_ST (RO) The masked interrupt status status of the I2C_ARBITRATION_LOST_INT interrupt.
I2C_MST_TXFIFO_UDF_INT_ST (RO) The masked interrupt status status of I2C_TRAN_COMPLETE_INT interrupt.
I2C_TRAN_COMPLETE_INT_ST (RO) The masked interrupt status status of the I2C_TRAN_COMPLETE_INT interrupt.
I2C_TIME_OUT_INT_ST (RO)     The masked interrupt status status of the I2C_TIME_OUT_INT interrupt.
I2C_TRAN_START_INT_ST (RO)   The masked interrupt status status of the I2C_TRAN_START_INT interrupt.
I2C_NACK_INT_ST (RO)         The masked interrupt status status of I2C_SLAVE_STRETCH_INT interrupt.
I2C_TXFIFO_OVF_INT_ST (RO)   The masked interrupt status status of I2C_TXFIFO_OVF_INT interrupt.

Continued on the next page...
```