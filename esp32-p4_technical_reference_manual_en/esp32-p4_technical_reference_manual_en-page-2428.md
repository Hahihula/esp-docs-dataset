

```markdown
Register 44.54. LP_I2C_INT_RAW_REG (0x0020)

| Bit | Field Name                                 | Description                                                                 |
|-----|--------------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                            | (reserved)                                                                  |
| 30  | LP_I2C_DET_START_INT_RAW                   | The raw interrupt status of LP_I2C_DET_START_INT.                           |
| 29  | LP_I2C_SCL_MAIN_STO_INT_RAW                | The raw interrupt status of LP_I2C_SCL_MAIN_STO_INT.                        |
| 28  | LP_I2C_SCL_SLT_STO_INT_RAW                 | The raw interrupt status of LP_I2C_SCL_SLT_STO_INT.                         |
| 27  | LP_I2C_RXFIFO_UDF_OVF_INT_RAW              | The raw interrupt status of LP_I2C_RXFIFO_UDF_OVF_INT.                      |
| 26  | LP_I2C_TXFIFO_NACK_TRANS_OUT_COMPLETE_INT_RAW | The raw interrupt status of LP_I2C_TXFIFO_NACK_TRANS_OUT_COMPLETE_INT.     |
| 25  | LP_I2C_TIME完整性_INT_RAW                  | The raw interrupt status of LP_I2C_TIME完整性_INT.                         |
| 24  | LP_I2C_MST_TXFIFO_UDF_INT_RAW              | The raw interrupt status of LP_I2C_MST_TXFIFO_UDF_INT.                      |
| 23  | LP_I2C_ARBITRATION_LOST_INT_RAW            | The raw interrupt status of the LP_I2C_ARBITRATION_LOST_INT interrupt.      |
| 22  | LP_I2C_BYTE_TRANS_DONE_INT_RAW             | The raw interrupt status of the LP_I2C_BYTE_TRANS_DONE_INT interrupt.       |
| 21  | LP_I2C_END_DETECT_INT_RAW                  | The raw interrupt status of the LP_I2C_END_DETECT_INT interrupt.            |
| 20  | LP_I2C_RXFIFO_OVF_INT_RAW                  | The raw interrupt status of LP_I2C_RXFIFO_OVF_INT interrupt.                |
| 19  | LP_I2C_TXFIFO_WM_INT_RAW                   | The raw interrupt status of LP_I2C_TXFIFO_WM_INT interrupt.                 |
| 18  | LP_I2C_RXFIFO_WM_INT_RAW                   | The raw interrupt status of LP_I2C_RXFIFO_WM_INT interrupt.                 |
| 17  | LP_I2C_END_DETECT_INT_RAW                  | The raw interrupt status of the LP_I2C_END_DETECT_INT interrupt.            |
| 16  | LP_I2C_ARBITRATION_LOST_INT_RAW            | The raw interrupt status of the LP_I2C_ARBITRATION_LOST_INT interrupt.      |
| 15  | LP_I2C_BYTE_TRANS_DONE_INT_RAW             | The raw interrupt status of the LP_I2C_BYTE_TRANS_DONE_INT interrupt.       |
| 14  | LP_I2C_END_DETECT_INT_RAW                  | The raw interrupt status of the LP_I2C_END_DETECT_INT interrupt.            |
| 13  | LP_I2C_RXFIFO_OVF_INT_RAW                  | The raw interrupt status of LP_I2C_RXFIFO_OVF_INT interrupt.                |
| 12  | LP_I2C_TXFIFO_WM_INT_RAW                   | The raw interrupt status of LP_I2C_TXFIFO_WM_INT interrupt.                 |
| 11  | LP_I2C_RXFIFO_WM_INT_RAW                   | The raw interrupt status of LP_I2C_RXFIFO_WM_INT interrupt.                 |
| 10  | LP_I2C_END_DETECT_INT_RAW                  | The raw interrupt status of the LP_I2C_END_DETECT_INT interrupt.            |
| 9   | LP_I2C_ARBITRATION_LOST_INT_RAW            | The raw interrupt status of the LP_I2C_ARBITRATION_LOST_INT interrupt.      |
| 8   | LP_I2C_BYTE_TRANS_DONE_INT_RAW             | The raw interrupt status of the LP_I2C_BYTE_TRANS_DONE_INT interrupt.       |
| 7   | LP_I2C_END_DETECT_INT_RAW                  | The raw interrupt status of the LP_I2C_END_DETECT_INT interrupt.            |
| 6   | LP_I2C_RXFIFO_OVF_INT_RAW                  | The raw interrupt status of LP_I2C_RXFIFO_OVF_INT interrupt.                |
| 5   | LP_I2C_TXFIFO_WM_INT_RAW                   | The raw interrupt status of LP_I2C_TXFIFO_WM_INT interrupt.                 |
| 4   | LP_I2C_RXFIFO_WM_INT_RAW                   | The raw interrupt status of LP_I2C_RXFIFO_WM_INT interrupt.                 |
| 3   | LP_I2C_END_DETECT_INT_RAW                  | The raw interrupt status of the LP_I2C_END_DETECT_INT interrupt.            |
| 2   | LP_I2C_ARBITRATION_LOST_INT_RAW            | The raw interrupt status of the LP_I2C_ARBITRATION_LOST_INT interrupt.      |
| 1   | LP_I2C_BYTE_TRANS_DONE_INT_RAW             | The raw interrupt status of the LP_I2C_BYTE_TRANS_DONE_INT interrupt.       |
| 0   | Reset                                      | Reset value: 0x00                                                           |

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

LP_I2C_TIME_OUT_INT_RAW The raw interrupt status of the LP_I2C_TIME_OUT_INT interrupt.
(R/SS/WTC)
```