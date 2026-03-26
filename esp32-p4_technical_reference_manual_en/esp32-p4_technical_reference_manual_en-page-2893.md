

```markdown
- 1: Add carrier wave only on valid signals.

## 57.3.4.4 Continuous TX Mode

The continuous TX mode can be enabled by setting `RMT_TX_CONTI_MODE_CHn`. In this mode, the transmitter transmits the pulse codes from RAM in loops:

* If an end-marker is encountered, the transmitter starts transmitting from the first data of the channel’s RAM again.
* If no end-marker is encountered, the transmitter starts transmitting from the first data again after the last data is transmitted.

If `RMT_TX_LOOP_CNT_EN_CHn` is set, the loop counting is incremented by 1 each time an end-marker is encountered. If the counting reaches the value set by `RMT_TX_LOOP_NUM_CHn`, an `RMT_CHn_TX_LOOP_INT` interrupt is generated. If `RMT_LOOP_STOP_EN_CHn` is set, the transmission stops immediately once an `RMT_CHn_TX_LOOP_INT` interrupt is generated, otherwise, the transmission will continue. In an end-maker, if its period[14:0] is 0, then the period of the previous data must satisfy:

$$
(57.3)
\quad \text{where } T_{apb\_clk} + 19 \times T_{rmt\_sclk} < \text{period} \times T_{clk\_div}
$$

The period of the other data only need to satisfy **non-zero** period relation.

## 57.3.4.5 Simultaneous TX Mode

RMT module supports multiple channels transmitting data simultaneously. To use this function, follow the steps below:

1. Configure `RMT_TX_SIM_CHn` to choose which multiple channels are used to transmit data simultaneously.
2. Set `RMT_TX_SIM_EN` to enable this transmission mode.
3. Set `RMT_TX_START_CHn` for each selected channel, to start data transmitting.

The transmission starts once the final channel is configured. RMT module also supports simultaneous transmission of channels 0 ~ 2’s RAM accessed by APB bus and channel 3’s RAM accessed by GDMA.

## 57.3.5 Receiver

### 57.3.5.1 Normal RX Mode

The receiver of channel `m` is controlled by `RMT_RX_EN_CHm`:

* 0: The receiver stops receiving data;
* 1: The receiver starts working.

When the receiver becomes active, it starts counting from the first edge of the signal, detecting signal levels and counting clock cycles the level lasts for. Each cycle count (period) is then written back to RAM together with the level information (level). When the receiver detects no change in a signal level for a number of clock cycles more than the value set by `RMT_IDLE_THRES_CHm`, the receiver will stop receiving data, return to idle state, and generate an `RMT_CHm_RX_END_INT` interrupt. Please note that `RMT_IDLE_THRES_CHm` should be
```