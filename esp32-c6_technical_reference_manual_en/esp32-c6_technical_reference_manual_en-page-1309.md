

```markdown
Chapter 37 Remote Control Peripheral (RMT)

GoBack

37.3.4.4 Continuous TX Mode

The continuous TX mode can be enabled by setting RMT_TX_CONTI_MODE_CHn. In this mode, the transmitter sends the pulse codes from RAM in loops:

* If an end-marker is encountered, the transmitter starts transmitting the first data of the channel's RAM again.
* If no end-marker is encountered, there are two possible situations. In normal TX mode (RMT_MEM_TX_WRAP_EN_CHn = 0), an error interrupt occurs because the RAM is empty without any data to transmit. In wrap TX mode (RMT_MEM_TX_WRAP_EN_CHn = 1), the transmitter starts transmitting the first data again after the last data is transmitted.

If RMT_TX_LOOP_CNT_EN_CHn is set, the loop counting is incremented by 1 each time an end-marker is encountered. If the counting reaches the value set by RMT_TX_LOOP_NUM_CHn, an RMT_CHn_TX_LOOP_INT interrupt is generated. If RMT_LOOP_STOP_EN_CHn is set, the transmission stops instantly after an RMT_CHn_TX_LOOP_INT interrupt is generated. Otherwise, the transmission continues. In an end-marker, if its period[14:0] is 0, then the period of the previous data must satisfy:

    6 × T_apb_clk + 12 × T_rmt_sclk < period × T_clk_div   (2)

The period of the other data only need to satisfy relation (1).

37.3.4.5 Simultaneous TX Mode

RMT module supports multiple channels transmitting data simultaneously. To use this function, follow the steps below:

1. Configure RMT_TX_SIM_CHn to choose which multiple channels are used to transmit data simultaneously;
2. Set RMT_TX_SIM_EN to enable this transmission mode;
3. Set RMT_TX_START_CHn for each selected channel to start data transmission.

The transmission starts once the final channel is configured. Due to hardware limitations, there is no guarantee that two channels can start sending data exactly at the same time. The interval between two channels starting transmitting data is within 3 × T_clk_div.

37.3.5 Receiver

37.3.5.1 Normal RX Mode

The receiver of channel m is controlled by RMT_RX_EN_CHm:

* 0: the receiver stops receiving data;
* 1: the receiver starts working.

When the receiver becomes active, it starts counting from the first edge of the signal, detecting signal levels and counting clock cycles the level lasts for. Each cycle count (period) is then written back to RAM together with the level information (level). When the receiver detects no change in a signal level for a number of clock cycles more than the value set by RMT_IDLE_THRES_CHm, the receiver stops receiving data, returns to idle state, and generates an RMT_CHm_RX_END_INT interrupt. Please note that RMT_IDLE_THRES_CHm should
```