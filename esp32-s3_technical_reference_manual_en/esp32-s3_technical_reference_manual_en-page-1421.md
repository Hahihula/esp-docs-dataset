**Chapter Title:**
Chapter 37 Remote Control Peripheral (RMT)

**Body Text with Code and Formulas:**

If `RMT_TX_LOOP_CNT_EN_CHn` is set, the loop counting is incremented by 1 each time an end-marker is encountered. If the counting reaches the value set by `RMT_TX_LOOP_NUM_CHn`, a RMT_CHn_TX_LOOP_INT interrupt is generated. If `RMT LOOP_STOP_EN_CHn` is set, the transmission stops immediately once an `RMT_CHn_TX_LOOP_INT` interrupt is generated; otherwise, the transmission will continue.

In an end-maker, if its period[14:0] is 0, then the period of the previous data must satisfy:

\[ \frac{6}{T_{apb\_clk}} + 12 \times T_{rmt\_sclk} < period \div T_{clk\_div} \]

The period of the other data only need to satisfy relation (1).

**Subsection Title:**
37.3.4.5 Simultaneous TX Mode

**Body Text with Steps and Instructions:**

RMT module supports multiple channels transmitting data simultaneously.

To use this function, follow these steps:

1. Configure `RMT_TX_SIM_CHn` to choose which multiple channels are used to transmit data simultaneously.
2. Set `RMT_TX_SIM_EN` to enable the transmission mode for each selected channel; start data transmitting by setting it on all desired channels (e.g., `RMT_TX_START_CHn`).
3. The transmission starts once the final channel is configured.

The RMT module also supports simultaneous transmissions of RAM accessed via APB bus and DMA access, with a range from 0 to 2's RAM for each selected channel (`RMT_TX_LOOP_NUM_CHn`).

**Subsection Title:**
37.3.5 Receiver

**Sub-subsection Title:**
37.3.5.1 Normal RX Mode

**Body Text with Instructions and Conditions:**

The receiver of `channel m` is controlled by `RMT_RX_EN_CHm`:

- 1: the receiver starts working.
- 0: the receiver stops receiving data.

When active, it counts from the first edge to detect signal levels. Each cycle count (period) written back RAM with level information (`level`). When no change in a number of clock cycles is detected for `RMT_IDLE_THRES_CHm`, return idle state and generate an interrupt if necessary; ensure that maximum value according application.

**Sub-subsection Title:**
37.3.5.2 Wrap RX Mode

**Body Text with Instructions on RAM Accessing:**

To receive more pulse codes, enable wrap mode for `channel m` by configuring `RMT_MEM_RX_WRAEN_CHm`. If accessed via DMA bus in wrap mode to send data larger than block size.

In wrap mode:

- Receiver stores received data into RAM space of channel.
- Ends when no change signal level detected; returns idle state and generates an interrupt if necessary. 

**Footer:**
Espressif Systems
1421 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback