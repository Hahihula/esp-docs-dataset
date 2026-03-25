
```markdown
Register 34.56. LP_I2C_INT_ENA_REG (0x002B)

| Bit | Field Name                             | Description                                                                 |
|-----|-----------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                         | Reset                                                                      |
| 30  | LP_I2C_RXFIFO_WM_INT_ENA               | Write 1 to enable LP_I2C_RXFIFO_WM_INT interrupt. (R/W)                     |
| 29  | LP_I2C_TXFIFO_WM_INT_ENA               | Write 1 to enable LP_I2C_TXFIFO_WM_INT interrupt. (R/W)                     |
| 28  | LP_I2C_RXFIFO_OVF_INT_ENA              | Write 1 to enable LP_I2C_RXFIFO_OVF_INT interrupt. (R/W)                    |
| 27  | LP_I2C_END_DETECT_INT_ENA              | Write 1 to enable the LP_I2C_END_DETECT_INT interrupt. (R/W)                |
| 26  | LP_I2C_BYTE_TRANS_DONE_INT_ENA         | Write 1 to enable the LP_I2C_BYTE_TRANS_DONE_INT interrupt. (R/W)           |
| 25  | LP_I2C_ARBITRATION_LOST_INT_ENA        | Write 1 to enable the LP_I2C_ARBITRATION_LOST_INT interrupt. (R/W)          |
| 24  | LP_I2C_MST_TXFIFO_UDF_INT_ENA          | Write 1 to enable LP_I2C_MST_TXFIFO_UDF_INT interrupt. (R/W)                |
| 23  | LP_I2C_TRANS_COMPLETE_INT_ENA          | Write 1 to enable the LP_I2C_TRANS_COMPLETE_INT interrupt. (R/W)            |
| 22  | LP_I2C_TIME_OUT_INT_ENA                | Write 1 to enable the LP_I2C_TIME_OUT_INT interrupt. (R/W)                  |
| 21  | LP_I2C_TRANS_START_INT_ENA             | Write 1 to enable the LP_I2C_TRANS_START_INT interrupt. (R/W)               |
| 20  | LP_I2C_NACK_INT_ENA                    | Write 1 to enable LP_I2C_NACK_INT interrupt. (R/W)                          |
| 19  | LP_I2C_TXFIFO_OVF_INT_ENA              | Write 1 to enable LP_I2C_TXFIFO_OVF_INT interrupt. (R/W)                    |
| 18  | LP_I2C_RXFIFO_UDF_INT_ENA              | Write 1 to enable LP_I2C_RXFIFO_UDF_INT interrupt. (R/W)                    |
| 17  | LP_I2C_SCL_ST_TO_INT_ENA               | Write 1 to enable LP_I2C_SCL_ST_TO_INT interrupt. (R/W)                     |
| 16  | LP_I2C_SCL_MAIN_ST_TO_INT_ENA          | Write 1 to enable LP_I2C_SCL_MAIN_ST_TO_INT interrupt. (R/W)                |
| 15  | LP_I2C_DET_START_INT_ENA               | Write 1 to enable LP_I2C_DET_START_INT interrupt. (R/W)                     |
```