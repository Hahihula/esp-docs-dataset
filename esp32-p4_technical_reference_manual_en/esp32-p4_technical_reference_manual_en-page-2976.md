

```markdown
1. The Touch FSM selects the touch sensor to be measured. The relevant signals are routed to that touch sensor.
2. The Touch FSM drives the START signal to the touch sensor to initiate the measurement. Internally, the Touch FSM starts a touch counter to time the duration of the measurement.
3. A pulse counter in the Touch FSM is incremented on each pulse received from the touch sensor's TOUCH_OUT signal.
4. When the pulse counter reaches the count threshold set in LP_ANA_TOUCH_MEAS_NUM0, the measurement is complete. The START signal is de-asserted, and the touch counter is stopped. The value of the stopped touch counter x LP_DYN_SLOW_CLK cycles indicates the time taken to charge and discharge the touch pin for LP_ANA_TOUCH_MEAS_NUM0 cycles.

• Frequency hopping enabled:

1. The Touch FSM selects the touch sensor to be measured. The relevant signals are routed to that touch sensor.
2. Set LP_ANA_FREQ_SCAN_EN to 1 to enable frequency hopping, configure LP_ANA_FREQ_SCAN_CNT_LIMIT to set the number of frequency modes supported for frequency hopping (up to three), and configure the parameters required for each frequency mode and the number of pulses for sampling the TOUCH_OUT signal.
3. The Touch FSM drives the START signal to the touch sensor to initiate the measurement. Internally, the Touch FSM starts a touch counter to time the duration of the measurement.
4. A pulse counter in the Touch FSM is incremented on each pulse received from the touch sensor's TOUCH_OUT signal.
5. When the pulse counter reaches the count threshold set in LP_ANA_TOUCH_MEAS_NUM0 of the corresponding frequency mode, the measurement is complete. The value of the stopped touch counter indicates the time taken to charge and discharge the touch pin LP_ANA_TOUCH_MEAS_NUM0 cycles with the current frequency.
6. The sampling frequency counter is incremented by 1 and the touch counter is cleared. The next frequency mode will be sampled after a small delay. When the samplings are finished for all frequency modes, the START signal is de-asserted, and the touch counter is cleared.

The sampled value (measured value) is the value of the touch counter indicated as touch_raw_data. The value of touch_raw_data can be read from RTC_TOUCH_PADn_DATA. Note that the value returned by RTC_TOUCH_PADn_DATA may also be the filtered touch_raw_data, i.e., touch_smooth_data and benchmark. Configure LP_ANA_TOUCH_DATA_SEL and LP_ANA_TOUCH_FREQ_SEL to select the type of the return value. For more information on the sampled value types and how to judge touch actions based on the data, refer to Section 60.4.3.1.

Note:
Note that if the pulse does not reach the set threshold for a long time while the touch counter has reached the timeout threshold set in LP_ANA_TOUCH_TIMEOUT_NUM with LP_ANA_TOUCH_TIMEOUT_EN set as 1, the RTC_TOUCH_TIMEOUT_INT_RAW timeout interrupt will be triggered, indicating a circuit abnormality.
```