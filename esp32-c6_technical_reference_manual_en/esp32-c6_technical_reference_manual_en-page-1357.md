

```markdown
| Signal          | Channel | ADC Selection |
|-----------------|---------|---------------|
| X32K_P (GPIO0)  | 0       |               |
| X32K_N (GPIO1)  | 1       |               |
| GPIO2           | 2       | SAR ADC       |
| GPIO3           | 3       |               |
| MTMS (GPIO4)    | 4       |               |
| MTDI (GPIO5)    | 5       |               |
| MTCK (GPIO6)    | 6       |               |

## 39.2.3.2 ADC Conversion and Attenuation

When the SAR ADC converts an analog voltage, the resolution (12-bit) of the conversion spans voltage range from 0 mV to $V_{ref}$. $V_{ref}$ is the SAR ADC's internal reference voltage (1100 mV by design). The output value of the conversion (data) is mapped to analog voltage $V_{data}$ using the following formula:

$$
V_{data} = \frac{V_{ref}}{4095} \times data
$$

In order to convert voltages larger than $V_{ref}$, input signals can be attenuated before being input into the SAR ADC. The attenuation can be configured to 0 dB, 2.5 dB, 6 dB, and 12 dB.

## 39.2.3.3 DIG ADC Controller

The clock of the DIG ADC controller is quite fast, thus the sample rate is high. This controller supports:

* up to 12-bit sampling resolution
* software-triggered one-time sampling
* timer-triggered multi-channel scanning

The configuration of a one-time sampling triggered by the software is as follows:

* Set `APB_SARADC_ONETIME_SAMPLE` to select SAR ADC to perform a one-time sampling.
* Configure `APB_SARADC_ONETIME_CHANNEL` to select a channel to sample.
* Configure `APB_SARADC_ONETIME_ATTEN` to set attenuation.
* Configure `APB_SARADC_ONETIME_START` to start the one-time sampling.

Upon completion of sampling, the `APB_SARADC_ADC_DONE_INT_RAW` interrupt is generated. Once this interrupt is detected, software can initiate reading of the sampled values from `APB_SARADC_ADC_DATA`.

If the timer-triggered multi-channel scanning is selected, follow the configuration below. Note that in this mode, the scan sequence is performed according to the configuration entered in the pattern table.
```