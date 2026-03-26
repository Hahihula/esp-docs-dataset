

```markdown
Figure 60.4-5. Sensing Area


* The maximum detection distance “d” is 16 cm and the sensing area “S” is 20 cm², where “d” is positively correlated with “S” as shown in Figure 60.4-5.
* Up to three touch pins can be configured to operate simultaneously in proximity mode.
* Frequency hopping is also supported in proximity mode.

In proximity mode, a touch sensor samples for a fixed number of times and accumulates the sample values. If the final cumulative value exceeds the configured threshold, a proximity object is considered to be detected and an interrupt will be triggered. Note that since the sample values are accumulated, the values introduced in Section 60.4.3.1, i.e., touch_raw_data, touch_smooth_data, and benchmark, will not be generated in proximity mode.

To operate in proximity mode:

* Configure a touch sensor to operate in proximity mode by setting LP_ANA_TOUCH_APPROACH_PAD0, LP_ANA_TOUCH_APPROACH_PAD1, or LP_ANA_TOUCH_APPROACH_PAD2.
* Configure LP_ANA_TOUCH_APPROACH_LIMIT to adjust the number of samplings to generate the cumulative value. The touch sensor contains an internal sample counter to record the number of samplings.
* Set the threshold value via LP_ANA_TOUCH_PADx_THy, where x (1-14) represents the touch pin index and y (0-2) represents the frequency mode configured in hopping frequency.
* When the sample counter reaches the number of samplings configured in LP_ANA_TOUCH_APPROACH_MEAS_NUMn:
    - If the cumulative value exceeds the threshold value, an interrupt will be triggered.
    - The sample counter and the cumulative value are reset to 0. The touch sensor restarts accumulating the sample values.

## 60.4.5 Sleep Mode

To reduce power consumption, the touch sensor also supports sleep mode. In sleep mode, users can designate one touch sensor to operate actively (hereinafter referred to as the sleeping touch sensor) to monitor whether a touch occurs in real time, while the remaining 13 touch sensors are all powered down in sleep mode. Once the sleeping touch sensor detects a touch or a touch release, it will generate an interrupt to wake up the rest of the touch sensors. The sleeping touch sensor also supports frequency hopping and
```