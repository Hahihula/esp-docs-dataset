

```markdown
|31|29|28|21|20|17|16|15|13|12|9|8|7|6|5|4|3|2|1|0|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
||3| |80| |5| |0| |0|1| |0| |0| |0| |0|Reset|

LP_ANA_TOUCH_NN_DISUPDATE_BENCHMARK_EN Configures whether to turn off the benchmark data correction.
0: Do not turn off
1: Turn off
(R/W)

LP_ANA_TOUCH_HYSTERESIS Configures the sampling hysteresis. (R/W)

LP_ANA_TOUCH_NN_THRESH Configures the out-of-phase noise_threshold. (R/W)

LP_ANA_TOUCH_NOISE_THRESH Configures the noise_threshold. (R/W)

LP_ANA_TOUCH_SMOOTH_LVL Configures the IIR filter module for touch_smooth_data.(R/W)

LP_ANA_TOUCH_JITTER_STEP Configures the jitter step in filter module 7 for generating benchmark data. (R/W)

LP_ANA_TOUCH_FILTER_MODE Configures the filter module for generating benchmark data. (R/W)

LP_ANA_TOUCH_FILTER_EN Configures whether to enable the filter module for generating benchmark data.
0: Disable
1: Enable
(R/W)

LP_ANA_TOUCH_NN_LIMIT Configures the number of consecutive sampling instances where the sampling value exceeds the out-of-phase noise_threshold. (R/W)

LP_ANA_TOUCH_APPROACH_LIMIT Configures the number of sampling in proximity mode. (R/W)

LP_ANA_TOUCH_DEBOUNCE_LIMIT Configures the number of consecutive sampling for detecting touch state changes. (R/W)
```