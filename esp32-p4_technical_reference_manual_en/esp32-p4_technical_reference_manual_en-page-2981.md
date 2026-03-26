

```markdown
| LP_ANA_TOUCH_FILTER_MODE | Type   | Formula                                                                 |
|--------------------------|--------|-------------------------------------------------------------------------|
| 0                        | IIR 1/4| 1/4 touch_raw_data + 3/4 benchmark                                    |
| 1                        | IIR 1/8| 1/8 touch_raw_data + 7/8 benchmark                                    |
| 2                        | IIR 1/16| 1/16 touch_raw_data + 15/16 benchmark                                 |
| 3                        | IIR 1/32| 1/32 touch_raw_data + 31/32 benchmark                                 |
| 4                        | IIR 1/64| 1/64 touch_raw_data + 63/64 benchmark                                 |
| 5                        | IIR 1/128| 1/128 touch_raw_data + 127/128 benchmark                             |
| 6                        | IIR 1/256| 1/256 touch_raw_data + 255/256 benchmark                             |
| 7                        | JITTER | touch_raw_data +/- LP_ANA_TOUCH_JITTER_STEP                           |

## 60.4.3.2 Hardware Touch Detection

In hardware touch detection, the touch sensor can detect finger touch or release and trigger an interrupt. To use hardware touch detection, the following key parameters need to be defined:

*   **finger_threshold**: The threshold value used to determine a touch or a touch interruption. finger_threshold is configured via LP_ANA_TOUCH_PADx_THy, where x (1-14) represents the touch pin index and y (0-2) represents the frequency mode configured in hopping frequency.
*   **noise_threshold**: Indicates the maximum threshold of the upward and downward fluctuation of touch_smooth_data. noise_threshold is configured via LP_ANA_TOUCH_NOISE_THRES.
*   **hysteresis**: Used to avoid touch misjudgments caused by fluctuations of touch_smooth_data around touch thresholds. The hysteresis value is configured via LP_ANA_TOUCH_HHYSTERESIS.

The finger_threshold and noise_threshold values are not absolute thresholds, but offsets from the benchmark value, while the hysteresis value is an offset from finger_threshold. This prevents from misdiagnosing the gradual or slow changes of touch_raw_data caused by environmental factors such as temperature, power, or noise as a touch action.

After a series of calculations and comparisons based on the above parameters, the touch sensor will output the touch results detected on the touch pins via interrupts. Each touch sensor corresponds to a control register LP_ANA_TOUCH_OUTEN to configure whether to output the detection result.

## 60.4.4 Proximity Mode

When an object such as a finger is close to, but not touching, a touch pin, a small change in capacitance occurs on the touch pin, which is much smaller than the change caused by a physical touch. Proximity mode allows for the detection of these small changes.
```