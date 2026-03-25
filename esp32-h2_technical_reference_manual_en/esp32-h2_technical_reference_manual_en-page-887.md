
```markdown
Register 30.22. I2C_INT_CLR_REG (0x0024)

| Bit | Field Name                                 | Description                                                                 |
|-----|--------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                |                                                                             |
| 30  | I2C_SLAVE_ADDR_UNMATCH_INT_CLR            | Write 1 to clear I2C_SLAVE_ADDR_UNMATCH_INT. (WT)                           |
| 29  | I2C_GENERAL_CALL_INT_CLR                  | Write 1 to clear I2C_GENERAL_CALL_INT. (WT)                                 |
| 28  | I2C_SLAVE_STRETCH_INT_CLR                 | Write 1 to clear I2C_SLAVE_STRETCH_INT. (WT)                                |
| 27  | I2C_DET_START_INT_CLR                     | Write 1 to clear I2C_DET_START_INT. (WT)                                    |
| 26  | I2C_SCL_ST_TO_INT_CLR                     | Write 1 to clear I2C_SCL_ST_TO_INT. (WT)                                    |
| 25  | I2C_TXFIFO_UDF_INT_CLR                    | Write 1 to clear I2C_TXFIFO_UDF_INT. (WT)                                   |
| 24  | I2C_RXFIFO_OVF_INT_CLR                    | Write 1 to clear I2C_RXFIFO_OVF_INT. (WT)                                   |
| 23  | I2C_NACK_INT_CLR                          | Write 1 to clear I2C_NACK_INT. (WT)                                        |
| 22  | I2C_TRANS_START_INT_CLR                   | Write 1 to clear I2C_TRANS_START_INT. (WT)                                  |
| 21  | I2C_TIME_OUT_INT_CLR                      | Write 1 to clear I2C_TIME_OUT_INT. (WT)                                     |
| 20  | I2C-byte_trans_done_int_clr               | Write 1 to clear I2C_BYTE_TRANS_DONE_INT. (WT)                              |
| 19  | I2C_END_DETECT_INT_CLR                    | Write 1 to clear I2C_END_DETECT_INT. (WT)                                   |
| 18  | I2C_RXFIFO_OVF_INT_CLR                    | Write 1 to clear I2C_RXFIFO_OVF_INT. (WT)                                   |
| 17  | I2C_TXFIFO_WM_INT_CLR                     | Write 1 to clear I2C_TXFIFO_WM_INT. (WT)                                    |
| 16  | I2C_RXFIFO_WM_INT_CLR                     | Write 1 to clear I2C_RXFIFO_WM_INT. (WT)                                    |
| 15  | I2C_MST_TXFIFO_UDF_INT_CLR                | Write 1 to clear I2C_MST_TXFIFO_UDF_INT. (WT)                               |
| 14  | I2C_ARBITRATION_LOST_INT_CLR              | Write 1 to clear I2C_ARBITRATION_LOST_INT. (WT)                             |
| 13  | I2C_BYTE_TRANS_DONE_INT_CLR               | Write 1 to clear I2C_BYTE_TRANS_DONE_INT. (WT)                              |
| 12  | I2C_END_DETECT_INT_CLR                    | Write 1 to clear I2C_END_DETECT_INT. (WT)                                   |
| 11  | I2C_RXFIFO_OVF_INT_CLR                    | Write 1 to clear I2C_RXFIFO_OVF_INT. (WT)                                   |
| 10  | I2C_TXFIFO_WM_INT_CLR                     | Write 1 to clear I2C_TXFIFO_WM_INT. (WT)                                    |
| 9   | I2C_NACK_INT_CLR                          | Write 1 to clear I2C_NACK_INT. (WT)                                         |
| 8   | I2C_TRANS_COMPLETE_INT_CLR                | Write 1 to clear I2C_TRANS_COMPLETE_INT. (WT)                               |
| 7   | I2C_MST_TXFIFO_UDF_INT_CLR                | Write 1 to clear I2C_MST_TXFIFO_UDF_INT. (WT)                               |
| 6   | I2C_ARBITRATION_LOST_INT_CLR              | Write 1 to clear I2C_ARBITRATION_LOST_INT. (WT)                             |
| 5   | I2C_BYTE_TRANS_DONE_INT_CLR               | Write 1 to clear I2C_BYTE_TRANS_DONE_INT. (WT)                              |
| 4   | I2C_END_DETECT_INT_CLR                    | Write 1 to clear I2C_END_DETECT_INT. (WT)                                   |
| 3   | I2C_RXFIFO_OVF_INT_CLR                    | Write 1 to clear I2C_RXFIFO_OVF_INT. (WT)                                   |
| 2   | I2C_TXFIFO_WM_INT_CLR                     | Write 1 to clear I2C_TXFIFO_WM_INT. (WT)                                    |
| 1   | I2C_RXFIFO_WM_INT_CLR                     | Write 1 to clear I2C_RXFIFO_WM_INT. (WT)                                    |
| 0   | Reset                                     |                                                                             |

```