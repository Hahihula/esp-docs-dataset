

```markdown
- Digital_reader: reads data from SAR ADC, driven by DIG ADC FSM
- Filter: filters ADC converted data in multi-channel sampling mode
- Threshold monitorx: threshold monitor 1 and threshold monitor 2. The monitorx will trigger an interrupt when the converted value is below a low threshold or above a high threshold.
```

## 46.5 Functional Description

### 46.5.1 ADC Power Up

The ADC can be powered up by setting PMU_XPD_PERIF_I2C and PMU_PERIF_I2C_RST. ADC sampling can be performed right after power-up. Users do not need to worry about wait time, as it has been dealt with in hardware design.

### 46.5.2 ADC Channels

The SAR ADC has six channels that are connected to six pins on the chip. In order to sample an analog signal, the SAR ADC must first select the analog pin to measure via an internal multiplexer.

Table 46.5-1 shows the pins used as ADC channels and the corresponding GPIO numbers.

**Table 46.5-1. SAR ADC Channels**

| Pin Name     | GPIO Number | ADC Channel |
|--------------|-------------|-------------|
| XTAL_32K_N   | GPIO1       | 0           |
| MTMS         | GPIO2       | 1           |
| MTDI         | GPIO3       | 2           |
| MTCK         | GPIO4       | 3           |
| MTDO         | GPIO5       | 4           |
| GPIO6        | GPIO6       | 5           |

### 46.5.3 ADC Clock

Figure 46.5-1 shows the clock structure of SAR ADC.

**Figure 46.5-1. SAR ADC Clock Structure**

```
      PCR_SARADC_CLKM_SEL
          |
XTAL_CLK ──► Clock mux ──► [Clock divider] ──► [Clock divider] → SAR_CLK
RC_FAST_CLK ────────────────► [Clock divider]
PLL_80M_CLK ────────────────► [Clock divider]

PCR_SARADC_CLKM_DIV_NUM
PCR_SAR1_CLK_DIV_NUM

ADC_CTRL_CLK (output from first clock divider)
```

Espressif Systems 1705 ESP32-C5 TRM (Version 1.0)
```