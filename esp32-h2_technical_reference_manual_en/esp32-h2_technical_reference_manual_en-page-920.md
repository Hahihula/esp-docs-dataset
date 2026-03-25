

```markdown
Register 31.3. I2S_INT_ENA_REG (0x0014)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  |                             | (reserved)                                                                  |
| 3   | I2S_RX_DONE_INT_ENA         | Write 1 to enable the I2S_RX_DONE_INT interrupt. (R/W)                      |
| 2   | I2S_TX_DONE_INT_ENA         | Write 1 to enable the I2S_TX_DONE_INT interrupt. (R/W)                      |
| 1   | I2S_RX_HUNG_INT_ENA         | Write 1 to enable the I2S_RX_HUNG_INT interrupt. (R/W)                      |
| 0   | I2S_TX_HUNG_INT_ENA         | Write 1 to enable the I2S_TX_HUNG_INT interrupt. (R/W)                      |

Register 31.4. I2S_INT_CLR_REG (0x0018)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  |                             | (reserved)                                                                  |
| 3   | I2S_RX_DONE_INT_CLR         | Write 1 to clear the I2S_RX_DONE_INT interrupt. (WT)                         |
| 2   | I2S_TX_DONE_INT_CLR         | Write 1 to clear the I2S_TX_DONE_INT interrupt. (WT)                         |
| 1   | I2S_RX_HUNG_INT_CLR         | Write 1 to clear the I2S_RX_HUNG_INT interrupt. (WT)                         |
| 0   | I2S_TX_HUNG_INT_CLR         | Write 1 to clear the I2S_TX_HUNG_INT interrupt. (WT)                         |
```