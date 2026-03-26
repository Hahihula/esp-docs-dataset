

# Chapter 62

## ADC Controller (ADC)

### 62.1 Overview

ESP32-P4 integrates two 12-bit successive approximation ADCs (SAR ADCs) for measuring analog signals from up to 14 pins. Figure 62.1-1 shows the basic architecture of the SAR ADC module on ESP32-P4.

Figure 62.1-1. SAR ADC Simplified Architecture

As the figure shows, the SAR ADCs are managed by four dedicated controllers:

*   Two HP (high-performance) controllers: HP ADC1 Controller and HP ADC2 Controller, designed for multi-channel sampling mode, supporting continuous transfer of conversion results to memory via the GDMA interface.
*   Two LP (low-power) controllers: LP ADC1 Controller and LP ADC2 Controller, supporting operation in sleep mode and one-shot sampling mode.