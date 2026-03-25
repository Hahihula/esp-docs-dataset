

```markdown
Register 30.24. I2C_INT_STATUS_REG (0x002C)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                    |                                                                             |
| 30  | I2C_SLAVE_ADDR_UNMATCH_INT_ST | The masked interrupt status of I2C_SLAVE_ADDR_UNMATCH_INT. (RO)              |
| 29  | I2C_GENERAL_CALL_INT_ST       | The masked interrupt status of I2C_GENERAL_CALL_INT.                        |
| 28  | I2C_SLAVE_STRETCH_INT_ST      | The masked interrupt status of I2C_SLAVE_STRETCH_INT.                       |
| 27  | I2C_DET_START_INT_ST          | The masked interrupt status of I2C_DET_START_INT.                           |
| 26  | I2C_SCL_MAIN_INT_ST           | The masked interrupt status of I2C_SCL_MAIN_INT.                            |
| 25  | I2C_SCL_STO_INT_ST            | The masked interrupt status of I2C_SCL_STO_INT.                             |
| 24  | I2C_RXFIFO_OVF_INT_ST         | The masked interrupt status of I2C_RXFIFO_OVF_INT.                          |
| 23  | I2C_TXFIFO_NACK_INT_ST        | The masked interrupt status of I2C_TXFIFO_NACK_INT.                         |
| 22  | I2C_TRAN_TIME_OUT_INT_ST      | The masked interrupt status of I2C_TRAN_TIME_OUT_INT.                       |
| 21  | I2C_MST_TXFIFO_UDE_INT_ST     | The masked interrupt status of I2C_MST_TXFIFO_UDE_INT.                      |
| 20  | I2C_BYTE_TRANS_COMPLETE_INT_ST| The masked interrupt status of I2C_BYTE_TRANS_COMPLETE_INT.                 |
| 19  | I2C_ARBITRATION_LOST_INT_ST   | The masked interrupt status of I2C_ARBITRATION_LOST_INT.                    |
| 18  | I2C_END_DETECT_INT_ST         | The masked interrupt status of I2C_END_DETECT_INT.                          |
| 17  | I2C_BYTE_TRANS_DONE_INT_ST    | The masked interrupt status of I2C_BYTE_TRANS_DONE_INT.                     |
| 16  | I2C_ARBITRATION_LOST_INT_ST   | The masked interrupt status of I2C_ARBITRATION_LOST_INT.                    |
| 15  | I2C_MST_TXFIFO_UDF_INT_ST     | The masked interrupt status of I2C_MST_TXFIFO_UDF_INT.                      |
| 14  | I2C_TRAN_COMPLETE_INT_ST      | The masked interrupt status of I2C_TRAN_COMPLETE_INT.                       |
| 13  | I2C_TIME_OUT_INT_ST           | The masked interrupt status of I2C_TIME_OUT_INT.                            |
| 12  | I2C_TRAN_START_INT_ST         | The masked interrupt status of I2C_TRAN_START_INT.                          |
| 11  | I2C_NACK_INT_ST               | The masked interrupt status of I2C_SLAVE_STRETCH_INT.                       |
| 10  | I2C_TXFIFO_OVF_INT_ST         | The masked interrupt status of I2C_TXFIFO_OVF_INT.                          |

I2C_RXFIFO_WM_INT_ST   The masked interrupt status of I2C_RXFIFO_WM_INT. (RO)
I2C_TXFIFO_WM_INT_ST   The masked interrupt status of I2C_TXFIFO_WM_INT. (RO)
I2C_RXFIFO_OVF_INT_ST  The masked interrupt status of I2C_RXFIFO_OVF_INT. (RO)
I2C_END_DETECT_INT_ST  The masked interrupt status of I2C_END_DETECT_INT. (RO)
I2C_BYTE_TRANS_DONE_INT_ST The masked interrupt status of I2C_END_DETECT_INT. (RO)
I2C_ARBITRATION_LOST_INT_ST The masked interrupt status of I2C_ARBITRATION_LOST_INT. (RO)
I2C_MST_TXFIFO_UDF_INT_ST The masked interrupt status of I2C_TRAN_COMPLETE_INT. (RO)
I2C_TRAN_COMPLETE_INT_ST The masked interrupt status of I2C_TRAN_COMPLETE_INT. (RO)
I2C_TIME_OUT_INT_ST    The masked interrupt status of I2C_TIME_OUT_INT. (RO)
I2C_TRAN_START_INT_ST  The masked interrupt status of I2C_TRAN_START_INT. (RO)
I2C_NACK_INT_ST        The masked interrupt status of I2C_SLAVE_STRETCH_INT. (RO)
I2C_TXFIFO_OVF_INT_ST  The masked interrupt status of I2C_TXFIFO_OVF_INT. (RO)

Continued on the next page...
```