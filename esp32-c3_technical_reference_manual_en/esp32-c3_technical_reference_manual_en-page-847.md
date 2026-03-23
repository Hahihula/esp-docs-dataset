

```markdown
Carrier wave can be added on all output signals during modulation, or just added on valid pulse codes (the data stored in RAM), depending on the configuration of RMT_CARRIER_EFF_EN_CHn:
* 0: add carrier wave on all output signals;
* 1: add carrier wave only on valid signals.

To implement the modulation configuration, please set RMT_CONF_UPDATE_CHn first. For more information, see Section 33.3.6.
```

```markdown
### 33.3.4.4 Continuous TX Mode

This continuous TX mode can be enabled by setting RMT_TX_CONTI_MODE_CHn. In this mode, the transmitter sends the pulse codes from RAM in loops.

* If an end-marker is encountered, the transmitter starts transmitting the first data again.
* If no end-marker is encountered, the transmitter starts transmitting the first data again after the last data is transmitted.

If RMT_TX_LOOP_CNT_EN_CHn is set, the loop counting is incremented by 1 each time an end-marker is encountered. If the counting reaches the value set in RMT_TX_LOOP_NUM_CHn, an RMT_CHn_TX_LOOP_INT is generated.

In an end-marker, if its period[14:0] is 0, then the period of the previous data must satisfy the following requirement:

6 × Tapb_clk + 12 × Trmt_sclk < period × Tclk_div (2)

The period of the other data only need to satisfy relation (1).

To implement the above-mentioned configuration, please set RMT_CONF_UPDATE_CHn first. For more information, see Section 33.3.6.
```

```markdown
### 33.3.4.5 Simultaneous TX Mode

RMT module supports multiple channels transmitting data simultaneously. To use this function, follow the steps below.

1. Configure RMT_TX_SIM_CHn to choose which multiple channels are used to transmit data simultaneously.
2. Set RMT_TX_SIM_EN to enable this transmission mode.
3. Set RMT_TX_START_CHn for each selected channel, to start data transmitting.

Once the last channel is configured, these channels start transmitting data simultaneously. Due to hardware limitations, there is no guarantee that two channels can start sending data exactly at the same time. The interval between two channels starting transmitting data is within 3 × Tclk_div.

To configure RMT_TX_SIM_EN, please set RMT_CONF_UPDATE_CHn first. For more information, see Section 33.3.6.
```

```markdown
### 33.3.5 Receiver
```