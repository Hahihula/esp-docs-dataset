

```markdown
Register 30.19. I2S_ETM_CONF_REG (0x0070)

| Bit Range | Field Name                     | Description                                                                                                                                                                                                 |
|-----------|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 31        |                                | (reserved)                                                                                                                                                                                                |
|           |                                 | I2S_ETM_RX_RECEIVE_WORD_NUM                                                                                                                                                                                  |
|           |                                 | I2S_ETM_TX_SEND_WORD_NUM                                                                                                                                                                                   |

I2S_ETM_TX_SEND_WORD_NUM Configures the threshold of triggering ETM I2S_TX_X_WORDS_SENT event. When sending word number of I2S_ETM_TX_SEND_WORD_NUM [9:0], I2S will trigger the corresponding ETM event. (R/W)

I2S_ETM_RX_RECEIVE_WORD_NUM Configures the threshold of triggering ETM I2S_RX_X_WORDS_RECEIVED event. When receiving word number of I2S_ETM_RX_RECEIVE_WORD_NUM [9:0], I2S will trigger the corresponding ETM event. (R/W)

Register 30.20. I2S_DATE_REG (0x0080)

| Bit Range | Field Name   | Description |
|-----------|--------------|-------------|
| 31        |              | (reserved) |
|           |              | I2S_DATE    |
|           |              |             |

I2S_DATE Version control register. (R/W)
```