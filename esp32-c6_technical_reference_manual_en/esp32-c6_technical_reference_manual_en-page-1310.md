

```markdown
be configured to a maximum value according to your application, otherwise a valid received level may be mistaken as a level in idle state. If the RAM space of this RX channel is used up by the received data, the receiver stops receiving data, and an RMT_CHm_ERR_INT interrupt is triggered by RAM FULL event.

### 37.3.5.2 Wrap RX Mode

To receive more pulse codes than can be fitted in the channel's RAM, users can enable wrap mode for channel `m` by configuring `RMT_MEM_RX_WRAP_EN_CHm`. In wrap mode, the receiver stores the received data to RAM space of this channel in loops. The receiving ends when the receiver detects no change in a signal level for a number of clock cycles more than the value set by `RMT_IDLE_THRES_CHm`. The receiver returns to idle state and generates an RMT_CHm_RX_END_INT interrupt. For example, if `RMT_MEM_SIZE_CHm` is set to 1, the receiver starts receiving data and stores the data to address `48 * m`, and then to higher RAM address. When the receiver finishes storing the received data to `(48 * (m + 1) - 1)`, the receiver continues receiving data and storing data to the address `48 * m` again, and the receiving ends when no change is detected on a signal level for more than `RMT_IDLE_THRES_CHm` clock cycles. Wrap mode is also applicable when `RMT_MEM_SIZE_CHm > 1`.

An RMT_CHm_RX_THR_EVENT_INT interrupt is generated when the size of received pulse codes is larger than or equal to the value set by `RMT_CHm_RX_LIM_REG`. In wrap mode, `RMT_CHm_RX_LIM_REG` can be set to a half or a fraction of the size of the channel's RAM block. When an RMT_CHm_RX_THR_EVENT_INT interrupt is detected, the already used RAM region can be updated by subsequent data.

### 37.3.5.3 RX Filtering

Users can enable the receiver to filter input signals by setting `RMT_RX_FILTER_EN_CHm` for channel `m`. The filter samples input signals continuously, and detects the signals which remain unchanged for a continuous `RMT_RX_FILTER_THRES_CHm` clk_cycles as valid. Otherwise, the signals will be detected as invalid. Only the valid signals can pass through the filter. The filter removes pulses with a length of less than `RMT_RX_FILTER_THRES_CHm` clk_cycles.

### 37.3.5.4 RX Demodulation

Users can enable RX demodulation on input signals or on filtered signals by setting `RMT_CARRIER_EN_CHm`. RX demodulation can be applied to high-level carrier wave or low-level carrier wave, depending on the configuration of `RMT_CARRIER_OUT_LV_CHm`:

*   0: demodulate low-level carrier wave;
*   1: demodulate high-level carrier wave.

Users can configure `RMT_CARRIER_HIGH_THRES_CHm` and `RMT_CARRIER_LOW_THRES_CHm` to set the thresholds to demodulate high-level carrier or low-level carrier. If the high-level of a signal lasts for less than `RMT_CARRIER_HIGH_THRES_CHm` clk_div cycles, or the low-level lasts for less than `RMT_CARRIER_LOW_THRES_CHm` clk_div cycles, the signal is detected as a carrier and is then filtered out.

### 37.3.6 Configuration Update

To update RMT registers configuration, please set `RMT_CONF_UPDATE_CHn/m` for each channel first. All the bits/fields listed in the second column of Table 37.3-1 should follow this rule.
```