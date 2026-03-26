

```markdown
Note:
Updating the configuration described in this and subsequent sections requires setting RMT_CONF_UPDATE_CHn/m first. See Section 57.3.6.
```

### 57.3.4.1 Normal TX Mode

When `RMT_TX_START_CHn` is set, the transmitter of channel `n` starts reading and transmitting pulse codes from the starting address of its RAM block. The codes are sent starting from low-address entry. When an end-marker (a zero period) is encountered, the transmitter stops the transmission, returns to idle state and generates an `RMT_CHn_TX_END_INT` interrupt. Setting `RMT_TX_STOP_CHn` to 1 also stops the transmission and immediately sets the transmitter back to idle. The output level of a transmitter in idle state is determined by the “level” field of the end-marker or by the content of `RMT_IDLE_OUT_LV_CHn`, depending on the configuration of `RMT_IDLE_OUT_EN_CHn`:

- 0: The level in idle state is determined by the “level” field of the end-marker;
- 1: The level is determined by `RMT_IDLE_OUT_LV_CHn`.

### 57.3.4.2 Wrap TX Mode

To transmit more pulse codes than that can be fitted in the channel’s RAM, users can enable wrap TX mode for channel `n` by setting `RMT_MEM_TX_WRAP_EN_CHn`. In this mode, the transmitter transmits the data from RAM in loops till an end-marker is encountered. For example, if `RMT_MEM_SIZE_CHn = 1`, the transmitter starts transmitting data from the address `48 x n`, and then the data from higher RAM address. Once the transmitter finishes transmitting data from `(48 x (n + 1) - 1)`, it continues transmitting data from `48 x n` again till an end-marker is encountered. Wrap mode is also applicable for `RMT_MEM_SIZE_CHn > 1`.

When the size of transmitted pulse codes is larger than or equal to the value set by `RMT_TX_LIM_CHn`, an `RMT_CHn_TX_THR_EVENT_INT` interrupt is generated. In wrap mode, `RMT_TX_LIM_CHn` can be set to a half or a fraction of the size of the channel’s RAM block. When an `RMT_CHn_TX_THR_EVENT_INT` interrupt is detected by software, the already used RAM region can be updated by new pulse codes. In such way, the transmitter can seamlessly transmit unlimited pulse codes in wrap mode.

Note:
If RAM is accessed by GDMA, more pulse codes than one block size can be transmitted with no additional operation needed. If accessed by APB bus, wrap mode has to be enabled via software to transmit more data than one block size.

### 57.3.4.3 TX Modulation

Transmitter output can be modulated with a carrier wave by setting `RMT_CARRIER_EN_CHn`. The carrier waveform is configurable. In a carrier cycle, the high level lasts for `(RMT_CARRIER_HIGH_CHn + 1) rmt_sclk` cycles, while the low level lasts for `(RMT_CARRIER_LOW_CHn + 1) rmt_sclk` cycles. When `RMT_CARRIER_OUT_LV_CHn` is set, carrier wave is added on the high-level of output signals; while `RMT_CARRIER_OUT_LV_CHn` is cleared, carrier wave is added on the low-level of output signals. Carrier wave can be added on all output signals during modulation, or just added on valid pulse codes (the data stored in RAM), which can be set by configuring `RMT_CARRIER_EFF_EN_CHn`:

- 0: Add carrier wave on all output signals;
```