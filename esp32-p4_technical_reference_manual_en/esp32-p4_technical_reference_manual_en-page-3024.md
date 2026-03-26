

```markdown
## 62.2 Terminology

The following terms related to SAR ADC are defined in the context of the ESP32-P4 Technical Reference Manual to help readers better understand this document:

- **SAR ADC**: Including analog ADC circuit and digital ADC controller. The HP ADC and LP ADC in the following text share the analog ADC circuit, but have their own controllers, namely the HP ADC controllers and LP ADC controllers. The SAR ADC mentioned in the text refers to both HP ADC and LP ADC.
- **HP ADC**: High-performance ADC, supporting multi-channel sampling, GDMA data transfer, etc., not available in sleep mode.
- **LP ADC**: Low-power ADC, supporting one-shot sampling mode, can be used in sleep mode.
- **One-shot sampling mode**: In this mode, LP ADC samples one channel at a time.
- **Multi-channel sampling mode**: In this mode, HP ADC sequentially samples a group of channels or continuously samples a single channel.
- **Dual HP ADC sampling**: It means two HP ADCs sample either simultaneously or alternatively.
- **Conversion result**: The conversion result is the binary digital value obtained after the analog-to-digital conversion process. It is sometimes written as conversion data.
- **Filtered data**: Filtered data is the result of processing conversion data through a filter.
- **Sampling**: The term typically refers to the entire process of sampling analog inputs, converting the sampled data, and transferring the conversion results to memory. In certain contexts and stages of the process, sampling may also refer to the SAR ADC capturing data points from an analog signal.

## 62.3 Features

The SAR ADCs have the following features:

- Support HP ADCx controllers and LP ADCx controllers to get control of SAR ADCx via software, x = 1, 2
- 12-bit resolution
- Analog inputs sampling from up to 14 pins
- **HP ADCx controllers:**
    - Provide multi-channel sampling control module, supporting multi-channel sampling mode, with configurable channel sampling sequence
    - Provide mode control module, supporting dual HP ADC sampling
    - Provide two filters with configurable filter coefficients
```