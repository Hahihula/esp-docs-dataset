

```markdown
Register 46.19. I2S_STATE_REG (0x006C)

I2S_TX_IDLE Represents the TX unit state.
0: I2S TX unit is working
1: I2S TX unit is in idle state
(RO)
```

```markdown
Register 46.20. I2S_ETM_CONF_REG (0x0070)

I2S_ETM_TX_SEND_WORD_NUM Configures the threshold of triggering ETM I2S_TX_X_WORDS_SENT event.
When transmitting word number of I2S_ETM_TX_SEND_WORD_NUM [9:0], I2S will trigger the corresponding ETM event. (R/W)

I2S_ETM_RX_RECEIVE_WORD_NUM Configures the threshold of triggering ETM I2S_RX_X_WORDS_RECEIVED event.
When receiving word number of I2S_ETM_RX_RECEIVE_WORD_NUM [9:0], I2S will trigger the corresponding ETM event.
(R/W)
```