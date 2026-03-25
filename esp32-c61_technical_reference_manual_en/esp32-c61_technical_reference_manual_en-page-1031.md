

```markdown
- I2S_RX_SLAVE_MOD  
  – 0: Master RX mode  
  – 1: Slave RX mode


## 28.8.1 Master/Slave TX Mode

- I2S works as a master transmitter:
  - Set `I2S_TX_START` to start transmitting data. When this bit is set, the TX unit keeps driving the clock signal and serial data.
  - If `I2S_TX_STOP_EN` is set and all the data in FIFO is transmitted, the master stops transmitting data and clock signals.
  - If `I2S_TX_STOP_EN` is cleared and all the data in FIFO is transmitted, meanwhile no new data is filled into FIFO, the TX unit keeps transmitting the last data frame and clock signal.
    – Master stops transmitting data when `I2S_TX_START` is cleared.

- I2S works as a slave transmitter:
  - Set `I2S_TX_START`. Wait for the master BCK clock to enable a transmit operation.
  - If `I2S_TX_STOP_EN` is set and all the data in FIFO is transmitted, then the slave keeps transmitting zeros, till the master stops providing BCK signal.
  - If `I2S_TX_STOP_EN` is cleared and all the data in FIFO is transmitted, meanwhile no new data is filled into FIFO, the TX unit keeps transmitting the last data frame.
  - If `I2S_TX_START` is cleared, slave keeps transmitting zeros till the master stops providing BCK clock signal.


## 28.8.2 Master/Slave RX Mode

- I2S works as a master receiver:
  - Set `I2S_RX_START` to start receiving data. When this bit is set, the RX unit keeps outputting clock signal and sampling input data.
  - Configure `I2S_RX_STOP_MODE` to control the suspension of data reception:
    * 0: The RX unit only suspends data reception when `I2S_RX_START` is cleared.
    * 1: The RX unit suspends data reception when `I2S_RX_START` is cleared or the number of received bytes is greater than the value configured in `I2S_RX_EOF_NUM_REG`. When `I2S_RX_START` is not cleared, data reception can be restarted by setting `I2S_RX_RESET` to 1.
    * 2: The RX unit suspends data reception when `I2S_RX_START` is cleared or GDMA RX FIFO is full. When `I2S_RX_START` is not cleared and the GDMA RX FIFO is no longer full, data reception can be restarted by setting `I2S_RX_RESET` to 1.
      – RX unit stops receiving data when `I2S_RX_START` is cleared.

- I2S works as a slave receiver:
  - Set `I2S_RX_START`. Wait for the master BCK signal to start receiving data.
```