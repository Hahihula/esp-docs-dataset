
```markdown
Register 44.24. I2C_INT_STATUS_REG (0x002C)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                     |                                                                             |
| 30  | I2C_SLAVE_ADDR_UNMATCH_INT_ST  | The masked interrupt status of I2C_SLAVE_ADDR_UNMATCH_INT. (RO)              |
| 29  | I2C_GENERAL_CALL_INT_ST        | The masked interrupt status of I2C_GENERAL_CALL_INT. (RO)                    |
| 28  | I2C_SLAVE_STRETCH_INT_ST       | The masked interrupt status of I2C_SLAVE_STRETCH_INT. (RO)                   |
| 27  | I2C_DET_START_INT_ST           | The masked interrupt status of I2C_DET_START_INT. (RO)                       |
| 26  | I2C_SCL_MAIN_INT_ST            | The masked interrupt status of I2C_SCL_MAIN_INT. (RO)                        |
| 25  | I2C_SCL_STO_INT_ST             | The masked interrupt status of I2C_SCL_STO_INT. (RO)                         |
| 24  | I2C_RXFIFO_OVF_INT_ST          | The masked interrupt status of I2C_RXFIFO_OVF_INT. (RO)                      |
| 23  | I2C_TXFIFO_UDF_INT_ST          | The masked interrupt status of I2C_TXFIFO_UDF_INT. (RO)                      |
| 22  | I2C_END_DETECT_INT_ST          | The masked interrupt status of I2C_END_DETECT_INT. (RO)                      |
| 21  | I2C_BYTE_TRANS_DONE_INT_ST     | The masked interrupt status of I2C_BYTE_TRANS_DONE_INT. (RO)                 |
| 20  | I2C_ARBITRATION_LOST_INT_ST    | The masked interrupt status of I2C_ARBITRATION_LOST_INT. (RO)                |
| 19  | I2C_MST_TXFIFO_UDF_INT_ST      | The masked interrupt status of I2C_MST_TXFIFO_UDF_INT. (RO)                  |
| 18  | I2C_TRANS_COMPLETE_INT_ST      | The masked interrupt status of I2C_TRANS_COMPLETE_INT. (RO)                  |
| 17  | I2C_TIME_OUT_INT_ST            | The masked interrupt status of I2C_TIME_OUT_INT. (RO)                        |
| 16  | I2C_TRANS_START_INT_ST         | The masked interrupt status of I2C_TRANS_START_INT. (RO)                     |
| 15  | I2C_NACK_INT_ST                | The masked interrupt status of I2C_SLAVE_STRETCH_INT. (RO)                   |
| 14  | I2C_TXFIFO_OVF_INT_ST          | The masked interrupt status of I2C_TXFIFO_OVF_INT. (RO)                      |

I2C_RXFIFO_WM_INT_ST   The masked interrupt status of I2C_RXFIFO_WM_INT interrupt. (RO)
I2C_TXFIFO_WM_INT_ST   The masked interrupt status of I2C_TXFIFO_WM_INT interrupt. (RO)
I2C_RXFIFO_OVF_INT_ST  The masked interrupt status of I2C_RXFIFO_OVF_INT interrupt. (RO)
I2C_END_DETECT_INT_ST  The masked interrupt status of the I2C_END_DETECT_INT interrupt. (RO)
I2C_BYTE_TRANS_DONE_INT_ST   The masked interrupt status of the I2C_END_DETECT_INT interrupt. (RO)
I2C_ARBITRATION_LOST_INT_ST   The masked interrupt status of the I2C_ARBITRATION_LOST_INT interrupt. (RO)
I2C_MST_TXFIFO_UDF_INT_ST     The masked interrupt status of I2C_TRANS_COMPLETE_INT interrupt. (RO)
I2C_TRANS_COMPLETE_INT_ST     The masked interrupt status of the I2C_TRANS_COMPLETE_INT interrupt. (RO)
I2C_TIME_OUT_INT_ST   The masked interrupt status of the I2C_TIME_OUT_INT interrupt. (RO)
I2C_TRANS_START_INT_ST   The masked interrupt status of the I2C_TRANS_START_INT interrupt. (RO)
I2C_NACK_INT_ST   The masked interrupt status of I2C_SLAVE_STRETCH_INT interrupt. (RO)
I2C_TXFIFO_OVF_INT_ST   The masked interrupt status of I2C_TXFIFO_OVF_INT interrupt. (RO)

Continued on the next page...
```