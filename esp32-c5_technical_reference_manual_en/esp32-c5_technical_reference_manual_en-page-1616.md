

```markdown
Chapter 42 Remote Control Peripheral (RMT)

GoBack

RMT_CARRIER_OUT_LV_CHn is cleared, carrier wave is added on the low-level of output signals. Carrier wave can be added on all output signals during modulation, or just added on valid pulse codes (the data stored in RAM), which can be set by configuring RMT_CARRIER_EFF_EN_CHn:

*   0: add carrier wave on all output signals;
*   1: add carrier wave only on valid signals.

42.3.4.4 Continuous TX Mode

The continuous TX mode can be enabled by setting RMT_TX_CONTI_MODE_CHn. In this mode, the transmitter transmits the pulse codes from RAM in loops:

*   If an end-marker is encountered, the transmitter starts transmitting the first data of the channel's RAM again.
*   If no end-marker is encountered, there are two possible situations. In normal TX mode (RMT_MEM_TX_WRAP_EN_CHn = 0), an error interrupt occurs because the RAM is empty without any data to transmit. In wrap TX mode (RMT_MEM_TX_WRAP_EN_CHn = 1), the transmitter starts transmitting the first data again after the last data is transmitted.

If RMT_TX_LOOP_CNT_EN_CHn is set, the loop counting is incremented by 1 each time an end-marker is encountered. If the counting reaches the value set by RMT_TX_LOOP_NUM_CHn, an RMT_CHn_TX_LOOP_INT interrupt is generated. If RMT_LOOP_STOP_EN_CHn is set, the transmission stops instantly after an RMT_CHn_TX_LOOP_INT interrupt is generated. Otherwise, the transmission continues. In an end-marker, if its period[14:0] is 0, then the period of the previous data must satisfy:

$$6 \times T_{apb\_clk} + 12 \times T_{rmt\_sclk} < period \times T_{clk\_div} \quad (2)$$

The period of the other data only need to satisfy relation (1).

42.3.4.5 Simultaneous TX Mode

RMT module supports multiple channels transmitting data simultaneously. To use this function, follow the steps below:

1.  Configure RMT_TX_SIM_CHn to choose which multiple channels are used to transmit data simultaneously;
2.  Set RMT_TX_SIM_EN to enable this transmission mode;
3.  Set RMT_TX_START_CHn for each selected channel to start data transmission.

The transmission starts once the final channel is configured. Due to hardware limitations, there is no guarantee that two channels can start transmitting data exactly at the same time. The interval between two channels starting transmitting data is within $3 \times T_{clk\_div}$.

42.3.5 Receiver

42.3.5.1 Normal RX Mode

The receiver of channel m is controlled by RMT_RX_EN_CHm:

*   0: the receiver stops receiving data;
```