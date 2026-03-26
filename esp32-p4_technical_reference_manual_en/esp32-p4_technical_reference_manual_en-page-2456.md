

```markdown
Note:

*   I2S_RX_BCK_DIV_NUM must not be configured as 1.
*   In I2S slave mode, make sure f_I2S_TX/RX_CLK >= 8 × f_BCK. The I2Sn module can output I2Sn_MCLK_out as the master clock for peripherals.

## 46.7 I2S Reset

The units and FIFOs in the I2Sn module are reset by the following bits.

*   I2Sn TX/RX units: Reset by the bits I2S_TX_RESET and I2S_RX_RESET;
*   I2Sn TX/RX FIFO: Reset by the bits I2S_TX_FIFO_RESET and I2S_RX_FIFO_RESET.

Note:

The I2Sn module clock must be configured first before the module and FIFO are reset.

## 46.8 I2S Master/Slave Mode

The ESP32-P4 I2Sn module can operate as a master or a slave in half-duplex and full-duplex communications, depending on the configuration of I2S_RX_SLAVE_MOD and I2S_TX_SLAVE_MOD.

*   **I2S_TX_SLAVE_MOD**
    - 0: Master TX mode
    - 1: Slave TX mode

*   **I2S_RX_SLAVE_MOD**
    - 0: Master RX mode
    - 1: Slave RX mode

### 46.8.1 Master/Slave TX Mode

*   I2Sn works as a master transmitter:
    *   Set I2S_TX_START to start transmitting data. When this bit is set, the TX unit keeps driving the clock signal and serial data.
    *   If I2S_TX_STOP_EN is set and all the data in FIFO is transmitted, the master stops transmitting data and clock signals.
    *   If I2S_TX_STOP_EN is cleared and all the data in FIFO is transmitted, meanwhile no new data is filled into FIFO, the TX unit keeps transmitting the last data frame and clock signal.
    *   Master stops transmitting data when the bit I2S_TX_START is cleared.

*   I2Sn works as a slave transmitter:
    *   Set I2S_TX_START. Wait for the master BCK clock to enable a transmit operation.
```