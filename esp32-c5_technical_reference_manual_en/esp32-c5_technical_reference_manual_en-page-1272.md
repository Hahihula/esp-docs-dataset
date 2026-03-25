

```markdown
Register 34.57. LP_I2C_INT_STATUS_REG (0x002C)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                             | Reset                                                                       |
| 30  |                                             |                                                                             |
| 29  |                                             |                                                                             |
| ... |                                             |                                                                             |
| 8   | LP_I2C_DET_START_INT_ST                    | The masked interrupt status of LP_I2C_DET_START_INT.ST                     |
| 7   | LP_I2C_SCL_ST_TO_INT_ST                    | The masked interrupt status of LP_I2C_SCL_ST_TO_INT.ST                      |
| 6   | LP_I2C_SCL_MAIN_ST_TO_INT_ST               | The masked interrupt status of LP_I2C_SCL_MAIN_ST_TO_INT.ST                 |
| 5   | LP_I2C_RXFIFO_OVF_INT_ST                   | The masked interrupt status of LP_I2C_RXFIFO_OVF_INT.ST                     |
| 4   | LP_I2C_TXFIFO_NAK_INT_ST                   | The masked interrupt status of LP_I2C_TXFIFO_NAK_INT.ST                     |
| 3   | LP_I2C_MST_TIME_OUT_INT_ST                 | The masked interrupt status of LP_I2C_MST_TIME_OUT_INT.ST                  |
| 2   | LP_I2C_MST_TRANS_COMPLETE_INT_ST           | The masked interrupt status of LP_I2C_MST_TRANS_COMPLETE_INT.ST            |
| 1   | LP_I2C_BYTE_RXFIFO_OVF_INT_ST              | The masked interrupt status of LP_I2C_BYTE_RXFIFO_OVF_INT.ST               |
| 0   | LP_I2C_RXFIFO_WM_INT_ST                    | The masked interrupt status of LP_I2C_RXFIFO_WM_INT.ST                      |

LP_I2C_RXFIFO_WM_INT_ST  The masked interrupt status of LP_I2C_RXFIFO_WM_INT (RO)

LP_I2C_TXFIFO_WM_INT_ST  The masked interrupt status of LP_I2C_TXFIFO_WM_INT (RO)

LP_I2C_RXFIFO_OVF_INT_ST The masked interrupt status of LP_I2C_RXFIFO_OVF_INT (RO)

LP_I2C_END_DETECT_INT_ST The masked interrupt status of the LP_I2C_END_DETECT_INT interrupt. (RO)

LP_I2C_BYTE_TRANS_DONE_INT_ST The masked interrupt status of the LP_I2C_BYTE_TRANS_DONE_INT interrupt. (RO)

LP_I2C_ARBITRATION_LOST_INT_ST The masked interrupt status of the LP_I2C_ARBITRATION_LOST_INT interrupt. (RO)

LP_I2C_MST_TXFIFO_UDF_INT_ST The masked interrupt status of LP_I2C_MST_TXFIFO_UDF_INT interrupt. (RO)

LP_I2C_TRANS_COMPLETE_INT_ST The masked interrupt status of the LP_I2C_TRANS_COMPLETE_INT interrupt. (RO)

LP_I2C_TIME_OUT_INT_ST   The masked interrupt status of the LP_I2C_TIME_OUT_INT interrupt. (RO)

LP_I2C_TRANS_START_INT_ST The masked interrupt status of the LP_I2C_TRANS_START_INT interrupt. (RO)

LP_I2C_NACK_INT_ST       The masked interrupt status of LP_I2C_NACK_INT interrupt. (RO)

LP_I2C_TXFIFO_OVF_INT_ST The masked interrupt status of LP_I2C_TXFIFO_OVF_INT interrupt. (RO)

LP_I2C_RXFIFO_UDF_INT_ST The masked interrupt status of LP_I2C_RXFIFO_UDF_INT interrupt. (RO)

LP_I2C_SCL_ST_TO_INT_ST  The masked interrupt status of LP_I2C_SCL_ST_TO_INT interrupt. (RO)
```