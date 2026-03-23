

```markdown
Chapter 33 Remote Control Peripheral (RMT)

GoBack

33.3.5.1 Normal RX Mode

The receiver of channel m is controlled by RMT_RX_EN_CHm:

*   RMT_RX_EN_CHm = 1, the receiver starts working.
*   RMT_RX_EN_CHm = 0, the receiver stops receiving data.

When the receiver becomes active, it starts counting from the first edge of the signal, detecting signal levels and counting clock cycles the level lasts for. Each cycle count is then written back to RAM.

When the receiver detects no change in a signal level for a number of clock cycles more than the value set by RMT_IDLE_THRES_CHm, the receiver will stop receiving data, return to idle state, and generate an RMT_CHm_RX_END_INT interrupt.

Please note that RMT_IDLE_THRES_CHm should be configured to a maximum value according to your application, otherwise a valid received level may be mistaken as a level in idle state.

If RAM block of this RX channel is used up by the received data, the receiver will stop receiving data, and generate an RMT_CHm_ERR_INT interrupt triggered by RAM FULL event.

To implement configuration above, please set RMT_CONF_UPDATE_CHm first. For more information, see Section 33.3.6.

33.3.5.2 Wrap RX Mode

To receive more pulse codes than can be fitted in the channel's RAM, users can enable wrap RX mode for channel m by configuring RMT_MEM_RX_WRAP_EN_CHm. In wrap mode, the receiver stores the received data to RAM block of this channel in loops.

Receiving ends, when the receiver detects no change in a signal level for a number of clock cycles more than the value set by RMT_IDLE_THRES_CHm. The receiver then returns to idle state and generates an RMT_CHm_RX_END_INT interrupt.

For example, if RMT_MEM_SIZE_CHm is set to 1, the receiver starts receiving data and stores the data to address 48 * m, and then to higher RAM address. When the receiver finishes storing the received data to address (48 * (m + 1) - 1), the receiver continues receiving data and storing data to the address 48 * m again, till no change is detected on a signal level for more than RMT_IDLE_THRES_CHm clock cycles. Wrap mode is also applicable for RMT_MEM_SIZE_CHm > 1.

An RMT_CHm_RX_THR_EVENT_INT is generated when the size of received pulse codes is larger than or equal to the value set by RMT_RX_LIM_CHm. In wrap mode, RMT_RX_LIM_CHM can be set to a half or a fraction of the size of the channel's RAM block. When an RMT_CHm_RX_THR_EVENT_INT interrupt is detected by software, the system will be notified to copy out data stored in already used RMT RAM region, and then the region can be updated by subsequent data. In this way an arbitrary amount of data can be seamlessly received.

To implement the configuration above, please set RMT_CONF_UPDATE_CHm first. For more information, see Section 33.3.6.

33.3.5.3 RX Filtering

Users can enable the receiver to filter input signals by setting RMT_RX_FILTER_EN_CHm for each channel. The filter samples input signals continuously, and detects the signals which remain unchanged for a
```