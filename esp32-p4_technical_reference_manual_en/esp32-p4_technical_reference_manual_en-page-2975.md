

```markdown
Chapter 60 Touch Sensor (TOUCH)

The following introduces the modules in the Touch FSM.

* SCAN_CTRL: Select the touch pin to measure, set the parameters such as hopping frequency, and controls the start and end of measurement for each touch sensor in scan mode.
* WORK_UNIT: Sample the selected touch sensors during a measurement.
* Filter: If enabled, each touch sensor can filter a series of measurements via an infinite impulse response (IIR) filter. The filtered value will be returned as the sampled value. See Section 60.4.3.1 for details.
* SCAN_CUR: Cache the parameters of different touch sensors at different frequency modes during the measurement to be used for the next measurement.

## 60.4.2 Sampled Signal Preprocessing

The core mechanism of the touch sensor is to reflect whether the touch panel is touched or not based on the change of the output pulse wave, i.e., the TOUCH_OUT signal, through detecting the change of capacitance on the touch panel. Therefore, the sampling of the TOUCH_OUT signal is critical. Figure 60.4-2 shows the preprocessing of the TOUCH_OUT signal.

![Figure 60.4-2. TOUCH_OUT Signal Preprocessing](image_path)

The frequency of TOUCH_OUT might be much higher than the sampling frequency. Therefore, in order to improve the accuracy of the signal sampling, users can divide the TOUCH_OUT signal by configuring LP_ANA_DIV_NUMn. n in this field represents different frequency modes in frequency hopping (refer to Section 60.4.2.4) with the value 0-2. The lowest bit configures whether to enable or disable frequency division. Set the lowest bit to 0 to disable frequency division, and set it to 1 to enable division. The highest two bits indicate the frequency division coefficient with a value of 0/1/2/3, corresponding to the 0/2/4/6 divisions.

If the frequency is still higher than twice the sampling frequency after frequency division, set LP_ANA_TOUCH_OUT_SEL to 1 to directly use the divided TOUCH_OUT signal as a clock. Set LP_ANA_TOUCH_OUT_GATE to configure whether to enable this clock.

### 60.4.2.1 Measurement Process

Depending on whether frequency hopping is enabled, a measurement of a touch pin can be divided into the following two processes:

* Frequency hopping not enabled:
```