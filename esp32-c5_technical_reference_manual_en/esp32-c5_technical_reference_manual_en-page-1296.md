

```markdown
35.9.3 Synchronous Counter

ESP32-C5 I2S TX unit contains synchronous counters to reflect the current I2S data transmission status. The counters can be used to detect I2S transmit data errors or to synchronize data when multiple devices are using I2S for data transmission.

ESP32-C5 I2S contains two types of synchronous counters:

*   **I2S_TX_FIFO_CNT**
    - Each time the I2S TX FIFO reads data, the counter is incremented by 1.
    - The counter can be reset by setting `I2S_TX_FIFO_CNT_RST`.
    - The counter is 31-bit wide and is automatically reset to zero on overflow.

*   **I2S_TX_BCK_CNT**
    - Each time I2S TX transmits a BCK cycle, the counter is incremented by 1.
    - The counter can be reset by setting `I2S_TX_BCK_CNT_RST`.
    - The counter is 31-bit wide and is automatically reset to zero on overflow.

Note:

-   Each time the I2S TX FIFO transmits data, a channel data is sent. Therefore, when I2S transmits the data correctly, `I2S_TX_BCK_CNT = I2S_TX_FIFO_CNT *` the bit width of channel TX data (see Section 35.9.1.4).
-   When the I2S TX unit transmits the data, there is some delay between fetching data from the FIFO and transmitting it to the line, so the value of `I2S_TX_BCK_CNT` might be a little different from that of `I2S_TX_FIFO_CNT`.

Application scenarios

1.  I2S TX synchronization for multiple devices
    When multiple devices transmit data through the I2S TX at the same time, desynchronization may occur after a long period of time due to small frequency differences in the clock sources. In this case, read the `I2S_TX_FIFO_CNT` value of each device to determine the location of the audio data being sent to perform synchronization.

2.  I2S TX stability check
    When the device is in an application scenario with high GDMA usage, there may be numbers missing in I2S TX occasionally due to multiplexing arbitration. In this case, check the ratio of `I2S_TX_BCK_CNT` to `I2S_TX_FIFO_CNT` to confirm the stability of the device when running I2S TX.

35.10 Receiving Data

In RX mode, I2S first reads data from the peripheral interface and then stores the data in memory via GDMA according to the configured channel mode and data mode.

35.10.1 Channel Mode Control

ESP32-C5 I2S supports both TDM RX mode and PDM RX mode. Set `I2S_RX_TDM_EN` to enable TDM RX mode, or set `I2S_RX_PDM_EN` to enable PDM RX mode.
```