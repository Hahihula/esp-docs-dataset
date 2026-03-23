

```markdown
## 34.2.3.7 ADC Filters

The DIG ADC controller provides two filters for automatic filtering of sampled ADC data. Both filters can be configured to any channel of either SAR ADC and then filter the sampled data for the target channel. The filter’s formula is shown below:

$$data_{cur} = \frac{(k - 1) data_{prev}}{k} + \frac{data_{in}}{k} + 0.5$$

- `data_cur`: the filtered data value.
- `data_in`: the sampled data value from the ADC.
- `data_prev`: the last filtered data value.
- `k`: the filter coefficient.

The filters are configured as follows:

- Configure `APB_SARADC_FILTER_CHANNELx` to select the ADC channel for filter x;
- Configure `APB_SARADC_FILTER_FACTORx` to set the coefficient for filter x;

Note that `x` is used here as the placeholder of filter index. O: filter 0; 1: filter 1.

## 34.2.3.8 Threshold Monitoring

DIG ADC controller contains two threshold monitors that can be configured to monitor on any channel of SAR ADC1 and SAR ADC2. A high threshold interrupt is triggered when the ADC sample value is larger than the pre-configured high threshold, and a low threshold interrupt is triggered if the sample value is lower than the pre-configured low threshold.

The configuration of threshold monitoring is as follows:

- Set `APB_SARADC_THRESHx_EN` to enable threshold monitor x.
- Configure `APB_SARADC_THRESHx_LOW` to set a low threshold;
- Configure `APB_SARADC_THRESHx_HIGH` to set a high threshold;
- Configure `APB_SARADC_THRESHx_CHANNEL` to select the SAR ADC and the channel to monitor.

Note that `x` is used here as the placeholder of monitor index. O: monitor 0; 1: monitor 1.

## 34.2.3.9 SAR ADC2 Arbiter

SAR ADC2 can be controlled by two controllers, namely, DIG ADC controller and PWDET controller. To avoid any possible conflicts and to improve the efficiency of SAR ADC2, ESP32-C3 provides an arbiter for SAR ADC2. The arbiter supports fair arbitration and fixed priority arbitration.

- Fair arbitration mode (cyclic priority arbitration) can be enabled by clearing `APB_SARADC_ADC_ARB_FIX_PRIORITY`.
- In fixed priority arbitration, users can set `APB_SARADC_ADC_ARB_APB_PRIORITY` (for DIG ADC controller) and `APB_SARADC_ADC_ARB_WIFI_PRIORITY` (for PWDET controller), to configure the priorities for these controllers. A larger value indicates a higher priority.
```