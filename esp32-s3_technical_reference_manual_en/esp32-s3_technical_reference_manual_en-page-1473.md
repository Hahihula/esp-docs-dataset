**Chapter Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**GoBack Link:** GoBack

---

**Section with Code Snippet (attenuation setting):**

```
atten write the value of 1 to this field, to set the attenuation to 2.5 dB.
ch_sel write the value of 0 to this field, to select channel 0 (see Table 39.3-1).
```

**Instructions:**
- Configure `APB_SARADC_SAR1_PATT_LEN` to 1, i.e., set pattern table length to (this value + 1 = 2). Then pattern table entries cmd0 and cmd1 for SAR ADC1 will be used.
- Enable the timer, then DIG ADC1 controller start scanning the channel 2 and channel O of SAR ADC1 in cycles, as configured in the pattern table entries.

**Subsection Title:**
39.3.7.6 DMA Data Format

**Body Text:** 
The SAR ADCs eventually pass 32-bit data to the DMA, see the figure below.
- Figure Caption:
  - **Figure 39.3-11. DMA Data Format**

**Figure Description (Data Layout):**
```
data
reserved
 reserved
 ch_sel
 reserved
 reserved
 reserved
0
xx
xxx x x x
```

**Subsection Title:**
39.3.7.7 ADC Filters

**Body Text:** 
The DIG ADC1 controller provide two filters for automatic filtering of sampled ADC data. Both filters can be configured to any two channels of SAR ADC and then filter the sampled data for the target channel. The filter's formula is shown below:

**Filter Formula:**
```
data_{cur} = \frac{(k-1) data_{prev}}{k} + \frac{data_{in}}{k} + 0.5
```

**Variables in Formula Explanation:** 
- `data_{cur}`: the filtered data value.
- `data_{in}`: the sampled data value from the SAR ADC.
- `data_{prev}`: the last filtered data value.
- `k`: the filter coefficient.

The filters are configured as follows:
- Configure `APB_SARADC_FILTER_CHANNELx` to select the SAR ADC channel for filter x;
- Configure `APB_SARADC_FILTER_FACTORx` to set the coefficient for filter x. 

Note that x is used here as the placeholder of filter index: 0: filter 0; 1: filter 1.

---

**Subsection Title:**
39.3.7.8 Threshold Monitoring

**Body Text:** 
DIG ADC1 controller contain two threshold monitors that can be configured to monitor on any channel of SAR ADC1. A high threshold interrupt is triggered when the ADC sample value is larger than the pre-configured high threshold, and a low threshold interrupt is triggered if the sample value is lower than the pre-configured low threshold.

**Footer:**
Espressif Systems
Page Number 1473

**Document Title:** ESP32-S3 TRM (Version 1.7)

**Feedback Link:** Submit Documentation Feedback