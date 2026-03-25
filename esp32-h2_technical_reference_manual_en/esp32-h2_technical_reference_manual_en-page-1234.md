

```markdown
# Chapter 40

## ADC Controller (ADC)

### 40.1 Overview

The 12-bit ADC is a successive approximation analog-to-digital converter. It has five channels allowing it to measure analog signals from five pins. The SAR ADC is managed by the DIG ADC controller that drives ADC sampling. The SAR ADC supports one-shot sampling and multi-channel sampling.

### 40.2 Terminology

The following terms related to SAR ADC are defined in the context of the ESP32-H2 Technical Reference Manual to help readers better understand this document:

- **SAR ADC:** Including analog ADC circuit and digital ADC controller.
- **One-shot sampling mode:** In this mode, ADC samples one channel at a time.
- **Multi-channel sampling mode:** In this mode, ADC sequentially samples a group of channels or continuously samples a single channel.
- **Conversion result:** The conversion result is the binary digital value obtained after the analog-to-digital conversion process. It is sometimes written as conversion data.
- **Filtered data:** Filtered data is the result of processing conversion data through a filter.
- **Sampling:** The term typically refers to the entire process of sampling analog inputs, converting the sampled data, and transferring the conversion results to memory. In certain contexts and stages of the process, sampling may also refer to the SAR ADC capturing data points from an analog signal.

### 40.3 Features

The SAR ADC has the following features:

- 12-bit resolution
- Analog inputs sampling from up to five pins
- One-shot sampling mode and multi-channel sampling mode
- Multi-channel sampling mode supports:
    - configurable channel sampling sequence
```