

```markdown
## 35.8 I2S Master/Slave Mode

The ESP32-C5 I2S module can operate as a master or a slave in half-duplex and full-duplex communications, depending on the configuration of `I2S_RX_SLAVE_MOD` and `I2S_TX_SLAVE_MOD`.

- **`I2S_TX_SLAVE_MOD`**
  - 0: Master TX mode
  - 1: Slave TX mode

- **`I2S_RX_SLAVE_MOD`**
  - 0: Master RX mode
  - 1: Slave RX mode


### 35.8.1 Master/Slave TX Mode

- I2S works as a master transmitter:
  - Set `I2S_TX_START` to start transmitting data. When this bit is set, the TX unit keeps driving the clock signal and serial data.
  - If `I2S_TX_STOP_EN` is set and all the data in FIFO is transmitted, the master stops transmitting data and clock signals.
  - If `I2S_TX_STOP_EN` is cleared and all the data in FIFO is transmitted, meanwhile no new data is filled into FIFO, the TX unit keeps transmitting the last data frame and clock signal.
  - Master stops transmitting data when `I2S_TX_START` is cleared.

- I2S works as a slave transmitter:
  - Set `I2S_TX_START`. Wait for the master BCK clock to enable a transmit operation.
  - If `I2S_TX_STOP_EN` is set and all the data in FIFO is transmitted, then the slave keeps transmitting zeros, till the master stops providing BCK signal.
  - If `I2S_TX_STOP_EN` is cleared and all the data in FIFO is transmitted, meanwhile no new data is filled into FIFO, the TX unit keeps transmitting the last data frame.
  - If `I2S_TX_START` is cleared, slave keeps transmitting zeros till the master stops providing BCK clock signal.


### 35.8.2 Master/Slave RX Mode

- I2S works as a master receiver:
  - Set `I2S_RX_START` to start receiving data. When this bit is set, the RX unit keeps outputting clock signal and sampling input data.
  - Configure `I2S_RX_STOP_MODE` to control the suspension of data reception:
    * 0: The RX unit only suspends data reception when `I2S_RX_START` is cleared.
```