

```markdown
Register 29.54. LP_I2C_INT_RAW_REG (0x0020)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 30  | LP_I2C_DET_START_INT_RAW       | The raw interrupt status of LP_I2C_DET_START_INT.                           |
| 29  | LP_I2C_SCL_MAIN_STO_INT_RAW    | The raw interrupt status of LP_I2C_SCL_MAIN_STO_INT.                        |
| 28  | LP_I2C_SCL_SLT_STO_INT_RAW     | The raw interrupt status of LP_I2C_SCL_SLT_STO_INT.                         |
| 27  | LP_I2C_RXFIFO_UDF_OVF_RAW      | The raw interrupt status of LP_I2C_RXFIFO_UDF_OVF.                          |
| 26  | LP_I2C_TXFIFO_NACK_TRANS_OUT_COMPLETE_RAW | The raw interrupt status of LP_I2C_TXFIFO_NACK_TRANS_OUT_COMPLETE_INT.    |
| 25  | LP_I2C_TIME完整性_INT_RAW      | The raw interrupt status of LP_I2C_TIME完整性_INT.                          |
| 24  | LP_I2C_MST_TXFIFO_UDF_INT_RAW  | The raw interrupt status of LP_I2C_MST_TXFIFO_UDF_INT.                      |
| 23  | LP_I2C_ARBITRATION_LOST_INT_RAW | The raw interrupt status of the LP_I2C_ARBITRATION_LOST_INT interrupt.      |
| 22  | LP_I2C_BYTE_TRANS_DONE_INT_RAW | The raw interrupt status of the LP_I2C_BYTE_TRANS_DONE_INT interrupt.       |
| 21  | LP_I2C_END_DETECT_INT_RAW      | The raw interrupt status of the LP_I2C_END_DETECT_INT interrupt.            |
| 20  | LP_I2C_RXFIFO_OVF_INT_RAW      | The raw interrupt status of LP_I2C_RXFIFO_OVF_INT.                          |
| 19  | LP_I2C_TXFIFO_WM_INT_RAW       | The raw interrupt status of LP_I2C_TXFIFO_WM_INT.                           |
| 18  | LP_I2C_RXFIFO_WM_INT_RAW       | The raw interrupt status of LP_I2C_RXFIFO_WM_INT.                           |
| 17  | LP_I2C_TIME完整性_INT_RAW      | The raw interrupt status of the LP_I2C_TIME完整性_INT interrupt.            |

LP_I2C_RXFIFO_WM_INT_RAW The raw interrupt status of LP_I2C_RXFIFO_WM_INT interrupt.
(R/SS/WTC)

LP_I2C_TXFIFO_WM_INT_RAW The raw interrupt status of LP_I2C_TXFIFO_WM_INT interrupt.
(R/SS/WTC)

LP_I2C_RXFIFO_OVF_INT_RAW The raw interrupt status of LP_I2C_RXFIFO_OVF_INT interrupt.
(R/SS/WTC)

LP_I2C_END_DETECT_INT_RAW The raw interrupt status of the LP_I2C_END_DETECT_INT interrupt.
(R/SS/WTC)

LP_I2C_BYTE_TRANS_DONE_INT_RAW The raw interrupt status of the LP_I2C_END_DETECT_INT interrupt.
(R/SS/WTC)

LP_I2C_ARBITRATION_LOST_INT_RAW The raw interrupt status of the
LP_I2C_ARBITRATION_LOST_INT interrupt. (R/SS/WTC)

LP_I2C_MST_TXFIFO_UDF_INT_RAW The raw interrupt status of LP_I2C_TRANS_COMPLETE_INT interrupt.
(R/SS/WTC)

LP_I2C_TRANS_COMPLETE_INT_RAW The raw interrupt status of the
LP_I2C_TRANS_COMPLETE_INT interrupt. (R/SS/WTC)

LP_I2C_TIME完整性_INT_RAW The raw interrupt status of the LP_I2C_TIME完整性_INT interrupt.
(R/SS/WTC)
```