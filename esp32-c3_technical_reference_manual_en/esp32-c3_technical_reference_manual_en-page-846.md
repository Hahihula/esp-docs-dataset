

```markdown
RMT_DIV_CNT_CHn/m is used to configure the divider coefficient of internal clock divider for RMT channels.
The coefficient is normally equal to the value of RMT_DIV_CNT_CHn/m, except value 0 that represents
coefficient 256. The clock divider can be reset by clearing RMT_REF_CNT_RST_CHn/m. The clock generated
from the divider can be used by the counter (see Figure 33.3-1).

### 33.3.4 Transmitter

#### 33.3.4.1 Normal TX Mode

When `RMT_TX_START_CHn` is set, the transmitter of channel `n` starts reading and sending pulse codes from
the starting address of its RAM block. The codes are sent starting from low-address entry.

When an end-marker (a zero period) is encountered, the transmitter stops the transmission, returns to idle
state and generates an `RMT_CHn_TX_END_INT` interrupt. Setting `RMT_TX_STOP_CHn` to 1 also stops the
transmission and immediately sets the transmitter back to idle.

The output level of a transmitter in idle state is determined by the “level” field of the end-marker or by the
content of `RMT_IDLE_OUT_LV_CHn`, depending on the configuration of `RMT_IDLE_OUT_EN_CHn`.

To implement the above-mentioned configurations, please set `RMT_CONF_UPDATE_CHn` first. For more
information, see Section 33.3.6.

#### 33.3.4.2 Wrap TX Mode

To transmit more pulse codes than can be fitted in the channel’s RAM, users can enable wrap TX mode by
setting `RMT_MEM_TX_WRAP_EN_CHn`. In this mode, the transmitter sends the data from RAM in loops till an
end-marker is encountered.

For example, if `RMT_MEM_SIZE_CHn = 1`, the transmitter starts sending data from the address `48 * n`, and then
the data from higher RAM addresses. Once the transmitter finishes sending the data from `(48 * (n + 1) - 1)`, it
continues sending data from `48 * n` again till an end-marker is encountered. Wrap mode is also applicable for
`RMT_MEM_SIZE_CHn > 1`.

When the size of transmitted pulse codes is larger than or equal to the value set by `RMT_TX_LIM_CHn`, an
`RMT_CHn_TX_THR_EVENT_INT` interrupt is triggered. In wrap mode, `RMT_TX_LIM_CHn` can be set to a half or
a fraction of the size of the channel’s RAM block. When an `RMT_CHn_TX_THR_EVENT_INT` interrupt is
detected by software, the already used RAM region can be updated with new pulse codes. In this way the
transmitter can seamlessly send unlimited pulse codes in wrap mode.

To update the configuration of `RMT_MEM_TX_WRAP_EN_CHn`, `RMT_MEM_SIZE_CHn`, and `RMT_TX_LIM_CHn`,
please set `RMT_CONF_UPDATE_CHn` first. For more information, see Section 33.3.6.

#### 33.3.4.3 TX Modulation

Transmitter output can be modulated with a carrier wave by setting `RMT_CARRIER_EN_CHn`. The carrier
waveform is configurable.

In a carrier cycle, high level lasts for `(RMT_CARRIER_HIGH_CHn + 1)` rmt_sclk cycles, while low level lasts for
`(RMT_CARRIER_LOW_CHn + 1)` rmt_sclk cycles. When `RMT_CARRIER_OUT_LV_CHn` is set, carrier wave is
added on the high-level of output signals; while `RMT_CARRIER_OUT_LV_CHn` is cleared, carrier wave is added
on the low-level of output signals.
```