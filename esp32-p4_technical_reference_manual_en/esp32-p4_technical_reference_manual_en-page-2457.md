

```markdown
- If `I2S_TX_STOP_EN` is set and all the data in FIFO is transmitted, then the slave keeps transmitting zeros, till the master stops providing BCK signal.
- If `I2S_TX_STOP_EN` is cleared and all the data in FIFO is transmitted, meanwhile no new data is filled into FIFO, the TX unit keeps transmitting the last data frame.
- If `I2S_TX_START` is cleared, slave keeps transmitting zeros till the master stops providing BCK clock signal.

## 46.8.2 Master/Slave RX Mode

*   `I2Sn` works as a master receiver:
    - Set `I2S_RX_START` to start receiving data. When this bit is set, the RX unit keeps outputting clock signal and sampling input data.
    - Configure `I2S_RX_STOP_MODE` to control the suspension of data reception:

        *   0: The RX unit only suspends data reception when `I2S_RX_START` is cleared.
        *   1: The RX unit suspends data reception when `I2S_RX_START` is cleared or the number of received bytes is greater than the value configured in `I2S_RX_EOF_NUM_REG`. When `I2S_RX_START` is not cleared, data reception can be restarted by setting `I2S_RX_RESET` to 1.
        *   2: The RX unit suspends data reception when `I2S_RX_START` is cleared or GDMA RX FIFO is full. When `I2S_RX_START` is not cleared and the GDMA RX FIFO is no longer full, data reception can be restarted by setting `I2S_RX_RESET` to 1.

    - RX unit stops receiving data when the bit `I2S_RX_START` is cleared.

*   `I2Sn` works as a slave receiver:
    - Set `I2S_RX_START`. Wait for the master BCK signal to start receiving data.
    - Configure `I2S_RX_STOP_MODE` to control data reception suspension:

        *   0: The RX unit only suspends data reception when `I2S_RX_START` is cleared.
        *   1: The RX unit suspends data reception when the number of received bytes is greater than the value configured in `I2S_RX_EOF_NUM_REG`. When `I2S_RX_START` is not cleared, data reception can be restarted by setting `I2S_RX_RESET` to 1.
        *   2: The RX unit suspends data reception when `I2S_RX_START` is cleared or GDMA RX FIFO is full. When `I2S_RX_START` is not cleared and the GDMA RX FIFO is no longer full, data reception can be restarted by setting `I2S_RX_RESET` to 1.

    - The RX unit stops receiving data when the bit `I2S_RX_START` is cleared.

## 46.9 Transmitting Data

**Note:**
Updating the configuration described in this and subsequent sections requires to set `I2S_TX_UPDATE` accordingly to synchronize registers from APB clock domain to TX clock domain. For more detailed configurations, see Section 46.13.1.
```