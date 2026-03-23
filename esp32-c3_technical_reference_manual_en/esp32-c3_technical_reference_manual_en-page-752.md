

```markdown
Register 29.3. I2S_INT_ENA_REG (0x0014)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  |                             | (reserved)                                                                  |
| 30-0|                             | Reset                                                                       |

I2S_RX_DONE_INT_ENA The interrupt enable bit for I2S_RX_DONE_INT interrupt. (R/W)
I2S_TX_DONE_INT_ENA The interrupt enable bit for I2S_TX_DONE_INT interrupt. (R/W)
I2S_RX_HUNG_INT_ENA The interrupt enable bit for I2S_RX_HUNG_INT interrupt. (R/W)
I2S_TX_HUNG_INT_ENA The interrupt enable bit for I2S_TX_HUNG_INT interrupt. (R/W)

Register 29.4. I2S_INT_CLR_REG (0x0018)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  |                             | (reserved)                                                                  |
| 30-0|                             | Reset                                                                       |

I2S_RX_DONE_INT_CLR Set this bit to clear I2S_RX_DONE_INT interrupt. (WT)
I2S_TX_DONE_INT_CLR Set this bit to clear I2S_TX_DONE_INT interrupt. (WT)
I2S_RX_HUNG_INT_CLR Set this bit to clear I2S_RX_HUNG_INT interrupt. (WT)
I2S_TX_HUNG_INT_CLR Set this bit to clear I2S_TX_HUNG_INT interrupt. (WT)
```