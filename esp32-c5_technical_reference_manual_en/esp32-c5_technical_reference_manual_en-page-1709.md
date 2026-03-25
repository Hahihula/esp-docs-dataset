

```markdown
1: Channel 1
2: Channel 2
3: Channel 3
4: Channel 4
5: Channel 5

(reserved) Reserved

## Pattern Configuration Example

Note: When using multi-channel continuous sampling, the attenuation for each channel must be set to be consistent. In this example, two channels are selected for multi-channel sampling:

*   Channel 0, with an attenuation of 2.5 dB
*   Channel 2, with an attenuation of 2.5 dB

The detailed configuration is as follows:

*   Configure the first pattern (cmd0):

    Figure 46.5-6. cmd0 configuration

    `atten` write 1 to this field, to set the attenuation to 2.5 dB.

    `ch_sel` write 0 to this field, to select channel 0.

*   Configure the second pattern (cmd1):

    Figure 46.5-7. cmd1 Configuration

    `atten` write 1 to this field, to set the attenuation to 2.5 dB.

    `ch_sel` write 2 to this field, to select channel 2.

*   Configure APB_SARADC_SAR_PATT_LEN to 1. Then patterns cmd0 and cmd1 will be used.
*   Enable the timer so that the DIG ADC controller starts sampling the two channels periodically.

## 46.5.9 ADC Filters

The DIG ADC controller provides two filters for filtering ADC converted data in multi-channel sampling mode. Both filters can be configured to any ADC channel, but cannot be configured to the same channel. If the two filters are configured to the same channel, the first one takes effect.
```