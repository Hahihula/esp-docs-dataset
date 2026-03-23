

```markdown
Chapter 39 On-Chip Sensor and Analog Signal Processing
GoBack

* Configure `APB_SARADC_TIMER_TARGET` to set the trigger target for DIG ADC timer. When the timer counting reaches two times of the pre-configured cycle number, a sampling operation is triggered.
* Configure `APB_SARADC_TIMER_EN` to enable the timer.
* When the timer times out, it drives FSM to start sampling according to the pattern table.
* Sampled data is automatically stored in memory via DMA. An interrupt is triggered once the scan is completed.

Note:
One-time sampling and multi-channel scanning can not be configured to perform at the same time.

39.2.3.4 DMA Support

DIG ADC controller supports direct memory access via the peripheral DMA, which is triggered by DIG ADC timer. Users can switch the DMA data path to DIG ADC by configuring `APB_SARADC_APB_ADC_TRANS` via software. For specific DMA configuration, please refer to Chapter 4 GDMA Controller (GDMA).

39.2.3.5 DIG ADC FSM

Overview

Figure 39.2-2 shows the diagram of DIG ADC FSM.

Figure 39.2-2. Diagram of DIG ADC FSM

Wherein:
* Timer: a dedicated timer for DIG ADC controller to generate a sample_start signal.
```