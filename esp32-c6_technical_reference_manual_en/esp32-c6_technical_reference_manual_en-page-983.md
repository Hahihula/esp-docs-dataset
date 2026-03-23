

```markdown
- Wait for the master BCK clock to enable a transmit operation.
- If I2S_TX_STOP_EN is set and all the data in FIFO is transmitted, then the slave keeps sending zeros, till the master stops providing BCK signal.
- If I2S_TX_STOP_EN is cleared and all the data in FIFO is transmitted, meanwhile no new data is filled into FIFO, then the TX unit keeps sending the last data frame.
- If I2S_TX_START is cleared, slave keeps sending zeros till the master stops providing BCK clock signal.

### 30.8.2 Master/Slave RX Mode

*   I2S works as a master receiver:
    - Set I2S_RX_START to start receiving data.
        - RX unit keeps outputting clock signal and sampling input data.
        - RX unit stops receiving data when the bit I2S_RX_START is cleared.
*   I2S works as a slave receiver:
    - Set I2S_RX_START.
    - Wait for master BCK signal to start receiving data.
    - RX unit stops receiving data when the bit I2S_RX_START is cleared.

## 30.9 Transmitting Data

**Note:**
Updating the configuration described in this and subsequent sections requires to set I2S_TX_UPDATE accordingly to synchronize registers from APB clock domain to TX clock domain. For more detailed configuration, see Section 30.11.1.

In TX mode, I2S first reads data through DMA and sends these data out via output signals according to the configured data mode and channel mode.

### 30.9.1 Data Format Control

Data format is controlled in the following phases:

*   Phase I: read data from memory and write it to TX FIFO;
*   Phase II: read the data to send (TX data) from TX FIFO and convert the data according to the output data mode;
*   Phase III: clock out the TX data serially.

#### 30.9.1.1 Bit Width Control of Channel Valid Data

The bit width of valid data in each channel is determined by I2S_TX_BITS_MOD and I2S_TX_24_FILL_EN. For details, see the table below.
```