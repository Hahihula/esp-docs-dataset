
```markdown
Register 44.23. I2C_INT_ENA_REG (0x0028)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                     |                                                                             |
| 19  | I2C_SLAVE_ADDR_UNMATCH_INT_ENA | Write 1 to enable I2C_SLAVE_ADDR_UNMATCH_INT interrupt. (R/W)               |
| 18  | I2C_GENERAL_CALL_INT_ENA       | Write 1 to enable I2C_GENERAL_CALL_INT interrupt. (R/W)                     |
| 17  | I2C_SCL_ST_TO_INT_ENA          | Write 1 to enable I2C_SCL_ST_TO_INT interrupt. (R/W)                       |
| 16  | I2C_DET_START_INT_ENA          | Write 1 to enable I2C_DET_START_INT interrupt. (R/W)                       |
| 15  | I2C_SLAVE_STRETCH_INT_ENA      | Write 1 to enable I2C_SLAVE_STRETCH_INT interrupt. (R/W)                   |
| 14  | I2C_SCL_MAIN_ST_TO_INT_ENA     | Write 1 to enable I2C_SCL_MAIN_ST_TO_INT interrupt. (R/W)                  |
| 13  | I2C_TXFIFO_OVF_INT_ENA         | Write 1 to enable I2C_TXFIFO_OVF_INT interrupt. (R/W)                      |
| 12  | I2C_RXFIFO_UVF_INT_ENA         | Write 1 to enable I2C_RXFIFO_UVF_INT interrupt. (R/W)                      |
| 11  | I2C_NACK_INT_ENA               | Write 1 to enable I2C_NACK_INT interrupt. (R/W)                            |
| 10  | I2C_TRANS_COMPLETE_INT_ENA     | Write 1 to enable I2C_TRANS_COMPLETE_INT interrupt. (R/W)                  |
| 9   | I2C_MST_TXFIFO_UDF_INT_ENA     | Write 1 to enable I2C_MST_TXFIFO_UDF_INT interrupt. (R/W)                  |
| 8   | I2C_ARBITRATION_LOST_INT_ENA   | Write 1 to enable the I2C_ARBITRATION_LOST_INT interrupt. (R/W)             |
| 7   | I2C_BYTE_TRANS_DONE_INT_ENA    | Write 1 to enable the I2C_BYTE_TRANS_DONE_INT interrupt. (R/W)             |
| 6   | I2C_END_DETECT_INT_ENA         | Write 1 to enable the I2C_END_DETECT_INT interrupt. (R/W)                  |
| 5   | I2C_RXFIFO_OVF_INT_ENA         | Write 1 to enable I2C_RXFIFO_OVF_INT interrupt. (R/W)                      |
| 4   | I2C_TIME_OUT_INT_ENA           | Write 1 to enable the I2C_TIME_OUT_INT interrupt. (R/W)                    |
| 3   | I2C_TRANS_START_INT_ENA        | Write 1 to enable the I2C_TRANS_START_INT interrupt. (R/W)                 |
| 2   | I2C_TXFIFO_COMPLETE_INT_ENA    | Write 1 to enable the I2C_TXFIFO_COMPLETE_INT interrupt. (R/W)             |
| 1   | I2C_RXFIFO_WM_INT_ENA          | Write 1 to enable I2C_RXFIFO_WM_INT interrupt. (R/W)                       |
| 0   | I2C_TXFIFO_WM_INT_ENA          | Write 1 to enable I2C_TXFIFO_WM_INT interrupt. (R/W)                       |

```