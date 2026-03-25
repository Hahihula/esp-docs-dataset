

```markdown
- Filter: filters ADC converted data in multi-channel sampling mode
- Threshold monitorx: threshold monitor 1 and threshold monitor 2. The monitorx will trigger an interrupt when the converted value is below a low threshold or above a high threshold.

## 40.5 Functional Description

### 40.5.1 ADC Power Up

The ADC can be powered up by setting PMU_XPD_PERIF_I2C. ADC sampling can be performed right after power-up. Users do not need to worry about wait time, as it has been dealt with in hardware design.

### 40.5.2 ADC Channels

The SAR ADC has five channels that are connected to five pins on the chip. In order to sample an analog signal, the SAR ADC must first select the analog pin to measure via an internal multiplexer.

Table 40.5-1 shows the pins used as ADC channels and the corresponding GPIO numbers.

**Table 40.5-1. SAR ADC Channels**

| Pin Name | GPIO Number | ADC Channel |
|----------|-------------|-------------|
| GPIO1    | GPIO1       | 0           |
| MTMS     | GPIO2       | 1           |
| MTDO     | GPIO3       | 2           |
| MTCK     | GPIO4       | 3           |
| MTDI     | GPIO5       | 4           |

### 40.5.3 ADC Clock

Figure 40.5-1 shows the clock structure of SAR ADC.

**Figure 40.5-1. SAR ADC Clock Structure**

The system clock for SAR ADC is ADC_CTRL_CLK, which is the operating clock for DIG ADC FSM and other control logic (except APB interface and Digital_reader).

ADC_CTRL_CLK has three possible sources: XTAL_CLK, RC_FAST_CLK, and PLL_F96M_CLK, selected by PCR_SARADC_CLKM_SEL.
```