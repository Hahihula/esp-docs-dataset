

```markdown
- Arbiter: this arbiter determines which controller is selected as the ADC2's working controller, DIG ADC controller or PWDET controller.
- Digital_Reader0 (driven by DIG ADC FSM): reads data from SAR ADC1.
- Digital_Reader1 (driven by DIG ADC FSM): reads data from SAR ADC2.
- DIG ADC FSM: generates the signals required throughout the ADC sampling process.
- Threshold monitorx: threshold monitor 1 and threshold monitor 2. The monitorx will trigger a interrupt when the sampled value is greater than the pre-set high threshold or less than the pre-set low threshold.

The following sections describe the individual components in details.

### 34.2.3.1 Input Signals

In order to sample an analog signal, an SAR ADC must first select the analog pin to measure via an internal multiplexer. A summary of all the analog signals that may be sent to the SAR ADC module for processing by either ADC1 or ADC2 are presented in Table 34.2-1.

Table 34.2-1. SAR ADC Input Signals

| Signal   | Channel | ADC Selection |
|----------|---------|---------------|
| GPIO0    | 0       |               |
| GPIO1    | 1       |               |
| GPIO2    | 2       | SAR ADC1      |
| GPIO3    | 3       |               |
| GPIO4    | 4       |               |
| GPIO5    | 0       | SAR ADC2      |

### 34.2.3.2 ADC Conversion and Attenuation

When the SAR ADCs convert an analog voltage, the resolution (12-bit) of the conversion spans voltage range from 0 mV to $V_{ref}$. $V_{ref}$ is the SAR ADC's internal reference voltage (1100 mV by design). The output value of the conversion (data) is mapped to analog voltage $V_{data}$ using the following formula:

$$
V_{data} = \frac{V_{ref}}{4095} \times data
$$

In order to convert voltages larger than $V_{ref}$, input signals can be attenuated before being input into the SAR ADCs. The attenuation can be configured to 0 dB, 2.5 dB, 6 dB, and 12 dB.

### 34.2.3.3 DIG ADC Controller

The clock of the DIG ADC controller is quite fast, thus the sample rate is high. For more information, see Section ADC Characteristics in ESP32-C3 Series Datasheet.

This controller supports:

- up to 12-bit sampling resolution
- software-triggered one-time sampling
- timer-triggered multi-channel scanning
```