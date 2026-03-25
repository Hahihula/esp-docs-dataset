

```markdown
The system clock for SAR ADC is `ADC_CTRL_CLK`, which is the operating clock for DIG ADC FSM and other control logic (except APB interface and Digital_reader).

`ADC_CTRL_CLK` has three possible sources: `XTAL_CLK`, `RC_FAST_CLK`, and `PLL_80M_CLK`, selected by `PCR_SARADC_CLKM_SEL`.

`SAR_CLK` is the operating clock for SAR ADC and Digital_reader. It is divided from `ADC_CTRL_CLK` and must not exceed 5 MHz.

For more information about clocks, please refer to Chapter 9 Reset and Clock.
```

## 46.5.4 One-Shot Sampling Mode

In one-shot sampling mode, the ADC samples one channel once. This mode is started by software using `APB_SARADC_ONETIME_SAMPLE`. Once sampling is done, the conversion result is stored in `APB_SARADC_DATA`. To switch channels, configure `APB_SARADC_ONETIME_SAMPLE` once again.

## 46.5.5 Multi-Channel Sampling Mode

Multi-channel sampling mode is triggered by a timer that is specifically designed for SAR ADC. In this mode the ADC samples a group of channels according to the sequence defined in the pattern table. The multi-channel sampling mode can also be used for continuous sampling on one channel.

The timer is enabled by setting `APB_SARADC_TIMER_EN`. A trigger target for the timer needs to be configured with `APB_SARADC_TIMER_TARGET`. When the timer counts up to two times of `APB_SARADC_TIMER_TARGET`, a sampling operation is triggered. The timer is clocked from `ADC_CTRL_CLK`.

When sampling is complete, the timer resets to 0 and starts counting again. The conversion result is transferred to memory continuously via the GDMA interface.

**Note:**
The SAR ADC can only work under one operating mode at one time, either one-shot sampling mode or multi-channel sampling mode.

## 46.5.6 ADC Conversion and Attenuation

The SAR ADC can measure analog voltages from 0 mV to `V_ref`. `V_ref` is the SAR ADC’s internal reference voltage (1100 mV by design). The conversion result (`data`) is a 12-bit digital value, the raw data. To calculate the voltage `V_data` based on the raw data, please use the formula below:

```
V_data = (V_ref / k) × (data / 4095)
```

`k` is the coefficient corresponding to the configured attenuation.

To convert voltages larger than `V_ref`, apply attenuation to the input signals using `APB_SARADC_ONETIME_ATTEN`. The supported attenuation levels are:

*   0 dB (`k≈100%`)
*   2.5 dB (`k≈75%`)
```