

```markdown
Chapter 62 ADC Controller (ADC)

GoBack

* Enable the timer so that the HP ADC1 Controller starts sampling the two channels periodically.

## 62.5.8 Dual HP ADC Sampling Control

`ADC_WORK_MODE` controls how two HP ADCs work together:

*   0: Single HP ADC sampling, i.e., only one HP ADC samples. When a sampling request is triggered by the timer, `ADC_SAR_SEL` controls which FSM receives the sampling request:
    *   0: HP ADC FSM1, i.e., using HP ADC1 for sampling.
    *   1: HP ADC FSM2, i.e., using HP ADC2 for sampling.

*   1: Dual HP ADC simultaneous sampling. When a sampling request is triggered by the timer, both HP ADC FSM1 and HP ADC FSM2 receive the sampling request.

*   2: Dual HP ADC alternative sampling. When an odd number of sampling requests are triggered by the timer, HP ADC FSM1 receives the sampling request. When an even number of sampling requests are triggered by the timer, HP ADC FSM2 receives the sampling request.

## 62.5.9 HP ADC Filters

The HP `ADCx` controllers provide two filters for filtering conversion results in multi-channel sampling mode. Both filters can be configured to any HP ADC channel, but cannot be configured to the same channel. If the two filters are configured to the same channel, the first one takes effect.

The filtered data is determined by the following equation:

```latex
data_{cur} = \frac{(k - 1) data_{prev}}{k} + \frac{data_{in}}{k} + 0.5
```

*   `data_cur`: the filtered data
*   `data_in`: the conversion result
*   `data_prev`: the last filtered data
*   `k`: the filter coefficient

The filters are configured as follows:

*   Configure `ADC_FILTER_CHANNELx` to select the HP ADC channel for filter x, x=0, 1.
*   Configure `ADC_FILTER_FACTORx` to set the coefficient k for filter x, x=0, 1.

## 62.5.10 HP ADC Threshold Monitors

The HP `ADCx` controllers provide two threshold monitors to monitor the filtered data in multi-channel sampling mode. When the data is above the high threshold, a high threshold interrupt is triggered; when the data is below the low threshold, a low threshold interrupt is triggered. Both monitors can be configured to any HP ADC channel, but cannot be configured to the same channel.

Threshold monitors are configured as follows:

*   Set `ADC_THRESHx_EN` to enable threshold monitor x (x=0, 1).
*   Configure `ADC_THRESHx_LOW` to set a low threshold.
```