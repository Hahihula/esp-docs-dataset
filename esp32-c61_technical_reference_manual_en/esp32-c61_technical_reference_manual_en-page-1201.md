

```markdown
Chapter 33 ADC Controller

Pattern Configuration Example

Note: When using multi-channel continuous sampling, the attenuation for each channel must be set to be consistent. In this example, two channels are selected for multi-channel sampling:

* Channel 0, with an attenuation of 2.5 dB
* Channel 2, with an attenuation of 2.5 dB

The detailed configuration is as follows:

* Configure the first pattern (cmd0):

Figure 33.5-6. cmd0 configuration

```
|   | ch_sel | atten |
|---:|--------:|-------|
| reserved |    |     |
| 5 | 4 | 2 | 1 | 0 |
| 0 | 0 | 1 |

atten write 1 to this field, to set the attenuation to 2.5 dB.
ch_sel write 0 to this field, to select channel 0.

* Configure the second pattern (cmd1):

Figure 33.5-7. cmd1 Configuration

```
|   | ch_sel | atten |
|---:|--------:|-------|
| reserved |    |     |
| 5 | 4 | 2 | 1 | 0 |
| 0 | 2 | 1 |

atten write 1 to this field, to set the attenuation to 2.5 dB.
ch_sel write 2 to this field, to select channel 2.

* Configure APB_SARADC_SAR_PATT_LEN to 1. Then patterns cmd0 and cmd1 will be used.
* Enable the timer so that the DIG ADC controller starts sampling the two channels periodically.

33.5.9 ADC Filters

The DIG ADC controller provides two filters for filtering ADC converted data in multi-channel sampling mode. Both filters can be configured to any ADC channel, but not to the same one. If the two filters are configured to the same channel, the first one takes effect.

The filtered data is determined by the following equation:

data_cur = ((k - 1) * data_prev / k) + (data_in / k) + 0.5

* data_cur: the filtered data
* data_in: the ADC converted data
* data_prev: the last filtered data
```