

```markdown
Figure 20.8-3. PDM Channel Control Example

46.9.3 Synchronous Counter

ESP32-P4 I2Sn TX unit contains synchronous counters to reflect the current I2Sn data transmission status.
The counters can be used to detect I2Sn transmit data errors or to synchronize data when multiple devices are
using I2Sn for data transmission.

ESP32-P4 I2Sn contains two types of synchronous counters:

*   **I2S_TX_FIFO_CNT**
    - Each time the I2Sn TX FIFO reads data, the counter is incremented by 1.
    - The counter can be reset by setting `I2S_TX_FIFO_CNT_RST`.
    - The counter is 31-bit wide and is automatically reset to zero on overflow.

*   **I2S_TX_BCK_CNT**
    - Each time I2Sn TX transmits a BCK cycle, the counter is incremented by 1.
    - The counter can be reset by setting `I2S_TX_BCK_CNT_RST`.
    - The counter is 31-bit wide and is automatically reset to zero on overflow.

Note:

*   Each time the I2Sn TX FIFO transmits data, a channel data is sent. Therefore, when I2Sn transmits the data
correctly, `I2S_TX_BCK_CNT = I2S_TX_FIFO_CNT ×` the bit width of channel TX data (see Section 46.9.1.4).
*   When the I2Sn TX unit transmits the data, there is some delay between fetching data from the FIFO and transmitting
it to the line, so the value of `I2S_TX_BCK_CNT` might be a little different from that of `I2S_TX_FIFO_CNT`.

Application scenarios

1.  I2S TX synchronization for multiple devices

When multiple devices transmit data through the I2S TX at the same time, desynchronization may occur
after a long period of time due to small frequency differences in the clock sources. In this case, read the
```