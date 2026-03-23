
```markdown
- Configure `APB_SARADC_SAR_PATT_LEN` to 1, i.e., set pattern table length to (this value + 1 = 2). Then pattern table entries cmd0 and cmd1 will be used.
- Enable the timer, then DIG ADC controller starts scanning the two channels in cycles, as configured in the pattern table entries.

## DMA Data Format

The ADC eventually passes 32-bit data to the DMA. See the figure below.

![Figure 39.2-8. DMA Data Format](image)

```markdown
| Bit Position | 31         | ... | 17   | 16    | 15     | ch_sel (reserved) | 13 | 12    | (reserved) | data |
|--------------|------------|-----|------|-------|--------|-------------------|----|-------|------------|------|
| Value        | xx         | ... | x    | xxx   | x      | x                 | x  | x     |            | x    |
```

**data**: SAR ADC read value; 12-bit

**ch_sel**: Channel; 3-bit

### 39.2.3.6 ADC Filters

The DIG ADC controller provides two filters for automatic filtering of sampled ADC data. Both filters can be configured to any channel of the SAR ADC and then filter the sampled data for the target channel. The filter's formula is shown below:

```latex
data_{cur} = \frac{(k - 1) \cdot data_{prev}}{k} + \frac{data_{in}}{k} + 0.5
```

- `data_cur`: the filtered data value.
- `data_in`: the sampled data value from the ADC.
- `data_prev`: the last filtered data value.
- `k`: the filter coefficient.

The filters are configured as follows:

- Configure `APB_SARADC_FILTER_CHANNELx` to select the ADC channel for filter x.
- Configure `APB_SARADC_FILTER_FACTORx` to set the coefficient for filter x.

Note that x is used here as the placeholder of filter index. O: filter 0; 1: filter 1.

### 39.2.3.7 Threshold Monitoring

DIG ADC controller contains two threshold monitors that can be configured to monitor on any channel of the SAR ADC. A high threshold interrupt is triggered when the ADC sample value is larger than the pre-configured high threshold, and a low threshold interrupt is triggered if the sample value is lower than the pre-configured low threshold.

The configuration of threshold monitoring is as follows:

- Set `APB_SARADC_THRESHx_EN` to enable threshold monitor x;
- Configure `APB_SARADC_THRESHx_LOW` to set a low threshold;
```