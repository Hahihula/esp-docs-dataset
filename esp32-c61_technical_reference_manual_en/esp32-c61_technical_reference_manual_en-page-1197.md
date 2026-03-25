

```markdown
- Digital_reader: reads data from SAR ADC, driven by DIG ADC FSM
- Filter: filters ADC converted data in multi-channel sampling mode
- Threshold monitorx: threshold monitor 1 and threshold monitor 2. The monitorx will trigger an interrupt when the converted value is below a low threshold or above a high threshold.
```

## 33.5 Functional Description

### 33.5.1 ADC Power Up

The ADC can be powered up by setting PMU_XPD_PERIF_I2C and PMU_PERIF_I2C_RST. ADC sampling can be performed right after power-up. Users do not need to worry about wait time, as it has been dealt with in hardware design.

### 33.5.2 ADC Channels

The SAR ADC has four channels that are connected to four pins on the chip. In order to sample an analog signal, the SAR ADC must first select the analog pin to measure via an internal multiplexer.

Table 33.5-1 shows the pins used as ADC channels and the corresponding GPIO numbers.

Table 33.5-1. SAR ADC Channels

| Pin Name     | GPIO Number | ADC Channel |
|--------------|-------------|-------------|
| XTAL_32K_N   | GPIO1       | 0           |
| MTMS         | GPIO3       | 1           |
| MTDI         | GPIO4       | 2           |
| MTCK         | GPIO5       | 3           |

### 33.5.3 ADC Clock

Figure 33.5-1 shows the clock structure of SAR ADC.

![Figure 33.5-1. SAR ADC Clock Structure](image_path) <!-- Note: Actual image not included in text extraction -->

The system clock for SAR ADC is ADC_CTRL_CLK, which is the operating clock for DIG ADC FSM and other control logic (except APB interface and Digital_reader).
```