
```markdown
Register 30.23. I2C_INT_ENA_REG (0x0028)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | I2C_SLAVE_ADDR_UNMATCH_INT_ENA                                             |
| 29  | I2C_GENERAL_CALL_INT_ENA                                                   |
| 28  | I2C_SLAVE_STRETCH_INT_ENA                                                  |
| 27  | I2C_DET_START_INT_STO_INT_ENA                                              |
| 26  | I2C_SCL_ST_TO_INT_ENA                                                       |
| 25  | I2C_TXFIFO_OVF_INT_ENA                                                     |
| 24  | I2C_RXFIFO_UOF_INT_ENA                                                     |
| 23  | I2C_NACK_INT_ENA                                                            |
| 22  | I2C_TRANS_START_INT_ENA                                                    |
| 21  | I2C_TIME_OUT_INT_ENA                                                       |
| 20  | I2C_TRANS_COMPLETE_INT_ENA                                                 |
| 19  | I2C_MST_TXFIFO_UOF_INT_ENA                                                 |
| 18  | I2C_ARBITRATION_LOST_INT_ENA                                               |
| 17  | I2C_BYTE_TRANS_DONE_INT_ENA                                                |
| 16  | I2C_END_DETECT_INT_ENA                                                     |
| 15  | I2C_RXFIFO_OVF_INT_ENA                                                     |
| 14  | I2C_TXFIFO_WM_INT_ENA                                                      |
| 13  | I2C_RXFIFO_WM_INT_ENA                                                      |
| 12  | Reset                                                                      |

I2C_RXFIFO_WM_INT_ENA   Write 1 to enable I2C_RXFIFO_WM_INT. (R/W)
I2C_TXFIFO_WM_INT_ENA   Write 1 to enable I2C_TXFIFO_WM_INT. (R/W)
I2C_RXFIFO_OVF_INT_ENA  Write 1 to enable I2C_RXFIFO_OVF_INT. (R/W)
I2C_END_DETECT_INT_ENA  Write 1 to enable the I2C_END_DETECT_INT. (R/W)
I2C_BYTE_TRANS_DONE_INT_ENA   Write 1 to enable I2C_END_DETECT_INT. (R/W)
I2C_ARBITRATION_LOST_INT_ENA  Write 1 to enable I2C_ARBITRATION_LOST_INT. (R/W)
I2C_MST_TXFIFO_UOF_INT_ENA    Write 1 to enable I2C_TRANS_COMPLETE_INT. (R/W)
I2C_TRANS_COMPLETE_INT_ENA   Write 1 to enable I2C_TRANS_COMPLETE_INT. (R/W)
I2C_TIME_OUT_INT_ENA          Write 1 to enable I2C_TIME_OUT_INT. (R/W)
I2C_TRANS_START_INT_ENA       Write 1 to enable I2C_TRANS_START_INT. (R/W)
I2C_NACK_INT_ENA              Write 1 to enable I2C_SLAVE_STRETCH_INT. (R/W)
I2C_TXFIFO_OVF_INT_ENA        Write 1 to enable I2C_TXFIFO_OVF_INT. (R/W)
I2C_RXFIFO_UOF_INT_ENA        Write 1 to enable I2C_RXFIFO_UOF_INT . (R/W)
I2C_SCL_ST_TO_INT_ENA         Write 1 to enable I2C_SCL_ST_TO_INT. (R/W)
I2C_SCL_MAIN_ST_TO_INT_ENA    Write 1 to enable I2C_SCL_MAIN_ST_TO_INT. (R/W)
I2C_DET_START_INT_ENA         Write 1 to enable I2C_DET_START_INT. (R/W)
I2C_SLAVE_STRETCH_INT_ENA     Write 1 to enable I2C_SLAVE_STRETCH_INT. (R/W)
I2C_GENERAL_CALL_INT_ENA      Write 1 to enable I2C_GENARAL_CALL_INT. (R/W)
I2C_SLAVE_ADDR_UNMATCH_INT_ENA Write 1 to enable I2C_SLAVE_ADDR_UNMATCH_INT. (R/W)
```