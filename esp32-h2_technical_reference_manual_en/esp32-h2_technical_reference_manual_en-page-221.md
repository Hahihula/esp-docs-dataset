

```markdown
Figure 6.4-2. GPIO Filter Timing of GPIO Input Signals


3. Glitch filter hardware supports eight channels, each of which selects one signal from the 19 (0 ~ 5, 8 ~ 14, 22 ~ 27) output signals from the GPIO Filter hardware and conducts the second-time filtering on the selected signal. This Glitch Filter hardware can be used to filter slow-speed signals. To enable this feature, follow the steps below:

* Configure `GPIO_EXT_FILTER_CHn_INPUT_IO_NUM` to m. n (0 ~ 7) represents the channel number.  
  m (0 ~ 5, 8 ~ 14, 22 ~ 27) represents the GPIO pin number.

* Configure `GPIO_EXT_FILTER_CHn_WINDOW_WIDTH` to VALUE1 and  
  `GPIO_EXT_FILTER_CHn_WINDOW_THRES` to VALUE2. During VALUE1 + 1 cycles, if there are VALUE2 + 1 input signals that do not match the current output signal value, the Glitch Filter hardware inverts the output signal. `GPIO_EXT_FILTER_CHn_WINDOW_WIDTH` and  
  `GPIO_EXT_FILTER_CHn_WINDOW_THRES` can be configured to the same value VALUE3, then only signals with a width greater than VALUE3 + 1 clock cycles will be sampled.

* Set `GPSD_FILTER_CHn_EN` to enable channel n.


An example is shown in Figure 6.4-3, where `GPIO_EXT_FILTER_CHx_WINDOW_WIDTH` is configured to 3 and `GPIO_EXT_FILTER_CHx_WINDOW_THRES` to 2. The output signal value (signal_out) keeps as "0" in the four clock cycles before T1. The input signal value (signal_in) has been "1" for three clock cycles in the same period, then the output signal is inverted to "1" after T1.

Figure 6.4-3. Glitch Filter Timing Example


4. Synchronize GPIO input signals. To do so, please set `GPIO_PINx_REG` corresponding to GPIO pin X as follows:

* Set `GPIO_PINx_SYNC1_BYPASS` to enable input signal synchronized on rising edge or on falling edge in the first-level synchronization, see Figure 6.4-1.

* Set `GPIO_PINx_SYNC2_BYPASS` to enable input signal synchronized on rising edge or on falling edge in the second-level synchronization, see Figure 6.4-1.
```