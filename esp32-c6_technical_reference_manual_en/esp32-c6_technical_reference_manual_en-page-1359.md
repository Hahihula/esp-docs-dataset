

```markdown
Chapter 39 On-Chip Sensor and Analog Signal Processing

GoBack

• pr: the pointer to pattern table entries. FSM sends out corresponding signals based on the configuration of the pattern table entry that the pointer points to.

Execution of the sampling process is as follows:

• Configure APB_SARADC_TIMER_EN to enable the DIG ADC timer. The timeout event of this timer triggers an sample_start signal. This signal drives the FSM module to start sampling.

• When the FSM module receives the sample_start signal, it starts the following operations:
    – Power up SAR ADC.
    – Configure the ADC channel and attenuation based on the pattern table entry that the current pr points to.
    – Output the corresponding en_pad and atten signals to the analog side according to the configuration information.
    – Initiate the sar_start signal and start sampling.

• When the FSM module receives the reader_done signal from ADC Reader (Digital_reader), it starts the following operations:
    – Stop sampling.
    – Transfer the data to the filter, and then threshold monitor transfers the data to memory via DMA (see Figure 39.2-1).
    – Update the pattern table pointer pr and wait for the next sampling. Note that if the pointer pr is smaller than APB_SARADC_SAR_PATT_LEN (table_length), then pr = pr + 1. Otherwise, pr is cleared.

Pattern Table

There is one pattern table in the controller, consisting of the APB_SARADC_SAR_PATT_TAB1_REG and APB_SARADC_SAR_PATT_TAB2_REG registers. See Figure 39.2-3 and Figure 39.2-4:

Figure 39.2-3. APB_SARADC_SAR_PATT_TAB1_REG and Pattern Table Entry 0 - Entry 3

| 31 | 24 | 23 | 18 | 17 | 12 | 11 | 6 | 5 | 0 |
|----|----|----|----|----|----|----|---|---|---|
| 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0x0000 | 0x0000 | 0x0000 |

cmd x represents pattern table entries. x here is the index numbered from 0 ~ 3.

Figure 39.2-4. APB_SARADC_SAR_PATT_TAB2_REG and Pattern Table Entry 4 - Entry 7

| 31 | 24 | 23 | 18 | 17 | 12 | 11 | 6 | 5 | 0 |
|----|----|----|----|----|----|----|---|---|---|
| 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0x0000 | 0x0000 | 0x0000 |

cmd x represents pattern table entries. x here is the index numbered from 4 ~ 7.
```