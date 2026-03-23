

```markdown
## 34.2.3.5 DMA Support

DIG ADC controller supports direct memory access via peripheral DMA, which is triggered by DIG ADC timer.
Users can switch the DMA data path to DIG ADC by configuring `APB_SARADC_APB_ADC_TRANS` via software.
For specific DMA configuration, please refer to Chapter 2 GDMA Controller (GDMA).

## 34.2.3.6 DIG ADC FSM

### Overview

Figure 34.2-2 shows the diagram of DIG ADC FSM.

| sar_sel | Channel[2:0] | Atten[1:0] |
|---------|--------------|------------|
| 0/1     | 0~4          | 0~3        |
| 0/1     | 0~4          | 0~3        |
| 0/1     | 0~4          | 0~3        |
| 0/1     | 0~4          | 0~3        |
| 0/1     | 0~4          | 0~3        |
| 0/1     | 0~4          | 0~3        |

![Figure 34.2-2. Diagram of DIG ADC FSM](image_path_if_available)

Wherein:

*   Timer: a dedicated timer for DIG ADC controller, to generate a sample_start signal.
*   pr: the pointer to pattern table entries. FSM sends out corresponding signals based on the configuration of the pattern table entry that the pointer points to.

The execution process is as follows:

*   Configure `APB_SARADC_TIMER_EN` to enable the DIG ADC timer. The timeout event of this timer triggers an sample_start signal. This signal drives the FSM module to start sampling.
*   When the FSM module receives the sample_start signal, it starts the following operations:
    *   Power up SAR ADC.
    *   Select SAR ADC1 or SAR ADC2 as the working ADC, configure the ADC channel and attenuation, based on the pattern table entry that the current pr points to.
    *   According to the configuration information, output the corresponding en_pad and atten signals to the analog side.
    *   Initiate the sar_start signal and start sampling.
```