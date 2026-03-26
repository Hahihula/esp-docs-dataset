

```markdown
• 0 dB (k≈100%)
• 2.5 dB (k≈75%)
• 6 dB (k≈50%)
• 12 dB (k≈25%)

## 62.5.5 HP ADC FSM

In multi-channel sampling mode HP ADC FSM (hereinafter referred to as FSM) generates all types of signals used in the sampling process. Figure 62.5-1 illustrates how the FSM works.

| Channel [5:2] | Atten [1:0] |
|---------------|-------------|
| 0~7           | 0~3         |
| 0~7           | 0~3         |
| 0~7           | 0~3         |
| 0~7           | 0~3         |
| 0~7           | 0~3         |
| 0~7           | 0~3         |

Figure 62.5-1. HP ADC FSM Block Diagram

Wherein:

• Timer: a dedicated timer for the HP ADC controller to generate `sample_start` signal.
• pr: a pointer to the pattern table that defines the conversion rules for HP ADC. FSM sends out corresponding signals based on the conversion rules.

Set `ADC_TIMER_EN` to enable the timer. The timeout event of this timer triggers a `sample_start` signal. This signal drives the FSM module to start sampling. When the FSM module receives the `sample_start` signal, it starts the following operations:

• Powers up HP ADC.
• Determines the conversion rules (selected sample channels and attenuations) defined in the patterns that the current pr points to.
• Outputs the `en_pin` and `atten` signals corresponding to the conversion rules to the analog side.
• Initiates the `sar_start` signal and starts sampling.
```