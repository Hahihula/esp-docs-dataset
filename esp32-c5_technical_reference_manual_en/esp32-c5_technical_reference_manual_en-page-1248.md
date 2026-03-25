

```markdown
Register 34.22. I2C_INT_CLR_REG (0x0024)

| Bit | Field Name                                 | Description                                                                 |
|-----|--------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                |                                                                             |
| 19  | I2C_SLAVE_ADDR_UNMATCH_INT_CLR            | Write 1 to clear I2C_SLAVE_ADDR_UNMATCH_INT interrupt. (WT)                 |
| 18  | I2C_GENERAL_CALL_INT_CLR                  | Write 1 to clear I2C_GENERAL_CALL_INT interrupt. (WT)                       |
| 17  | I2C_SCL_ST_TO_INT_CLR                     | Write 1 to clear I2C_SCL_ST_TO_INT interrupt. (WT)                          |
| 16  | I2C_SDA_DET_START_INT_CLR                 | Write 1 to clear I2C_DET_START_INT interrupt. (WT)                          |
| 15  | I2C_SDA_DET_ST_TO_INT_CLR                 | Write 1 to clear I2C_SDA_DET_ST_TO_INT interrupt. (WT)                      |
| 14  | I2C_SCL_MAIN_ST_TO_INT_CLR                | Write 1 to clear I2C_SCL_MAIN_ST_TO_INT interrupt. (WT)                     |
| 13  | I2C_SCL_ST_TO_INT_CLR                     | Write 1 to clear I2C_SCL_ST_TO_INT interrupt. (WT)                          |
| 12  | I2C_SDA_DET_START_INT_CLR                 | Write 1 to clear I2C_DET_START_INT interrupt. (WT)                          |
| 11  | I2C_SDA_DET_ST_TO_INT_CLR                 | Write 1 to clear I2C_SDA_DET_ST_TO_INT interrupt. (WT)                      |
| 10  | I2C_SCL_MAIN_ST_TO_INT_CLR                | Write 1 to clear I2C_SCL_MAIN_ST_TO_INT interrupt. (WT)                     |
| 9   | I2C_SCL_ST_TO_INT_CLR                     | Write 1 to clear I2C_SCL_ST_TO_INT interrupt. (WT)                          |
| 8   | I2C_SDA_DET_START_INT_CLR                 | Write 1 to clear I2C_DET_START_INT interrupt. (WT)                          |
| 7   | I2C_SCL_MAIN_ST_TO_INT_CLR                | Write 1 to clear I2C_SCL_MAIN_ST_TO_INT interrupt. (WT)                     |
| 6   | I2C_SCL_ST_TO_INT_CLR                     | Write 1 to clear I2C_SCL_ST_TO_INT interrupt. (WT)                          |
| 5   | I2C_SDA_DET_START_INT_CLR                 | Write 1 to clear I2C_DET_START_INT interrupt. (WT)                          |
| 4   | I2C_SCL_MAIN_ST_TO_INT_CLR                | Write 1 to clear I2C_SCL_MAIN_ST_TO_INT interrupt. (WT)                     |
| 3   | I2C_SCL_ST_TO_INT_CLR                     | Write 1 to clear I2C_SCL_ST_TO_INT interrupt. (WT)                          |
| 2   | I2C_SDA_DET_START_INT_CLR                 | Write 1 to clear I2C_DET_START_INT interrupt. (WT)                          |
| 1   | I2C_SCL_MAIN_ST_TO_INT_CLR                | Write 1 to clear I2C_SCL_MAIN_ST_TO_INT interrupt. (WT)                     |
| 0   | Reset                                     |                                                                             |

I2C_RXFIFO_WM_INT_CLR    Write 1 to clear I2C_RXFIFO_WM_INT interrupt. (WT)
I2C_TXFIFO_WM_INT_CLR    Write 1 to clear I2C_TXFIFO_WM_INT interrupt. (WT)
I2C_RXFIFO_OVF_INT_CLR   Write 1 to clear I2C_RXFIFO_OVF_INT interrupt. (WT)
I2C_END_DETECT_INT_CLR   Write 1 to clear the I2C_END_DETECT_INT interrupt. (WT)
I2C_BYTE_TRANS_DONE_INT_CLR Write 1 to clear the I2C_BYTE_TRANS_DONE_INT interrupt. (WT)
I2C_ARBITRATION_LOST_INT_CLR Write 1 to clear the I2C_ARBITRATION_LOST_INT interrupt. (WT)
I2C_MST_TXFIFO_UDF_INT_CLR Write 1 to clear I2C_MST_TXFIFO_UDF_INT interrupt. (WT)
I2C_TRANS_COMPLETE_INT_CLR Write 1 to clear the I2C_TRANS_COMPLETE_INT interrupt. (WT)
I2C_TIME_OUT_INT_CLR     Write 1 to clear the I2C_TIME_OUT_INT interrupt. (WT)
I2C_TRANS_START_INT_CLR  Write 1 to clear the I2C_TRANS_START_INT interrupt. (WT)
I2C_NACK_INT_CLR         Write 1 to clear I2C_NACK_INT interrupt. (WT)
I2C_TXFIFO_OVF_INT_CLR   Write 1 to clear I2C_TXFIFO_OVF_INT interrupt. (WT)
I2C_RXFIFO_UDF_INT_CLR   Write 1 to clear I2C_RXFIFO_UDF_INT interrupt. (WT)
```

Espressif Systems
1248
ESP32-C5 TRM (Version 1.0)

Submit Documentation Feedback