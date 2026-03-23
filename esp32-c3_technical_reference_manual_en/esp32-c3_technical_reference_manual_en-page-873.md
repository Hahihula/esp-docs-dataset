

```markdown
Chapter 34 On-Chip Sensor and Analog Signal Processing

GoBack

- When the FSM receives the reader_done signal from ADC Reader (Digital_Reader0 or Digital_Reader1), it will
    - stop sampling.
    - transfer the data to the filter, and then threshold monitor transfers the data to memory via DMA,
    - update the pattern table pointer pr and wait for the next sampling. Note that if the pointer pr is smaller than APB_SARADC_SAR_PATT_LEN (table_length), then pr = pr + 1, otherwise, pr is cleared.

Pattern Table

There is one pattern table in the controller, consisting of the APB_SARADC_SAR_PATT_TAB1_REG and APB_SARADC_SAR_PATT_TAB2_REG registers, see Figure 34.2-3 and Figure 34.2-4:

(reserved)

| 31 | 24 | 23 | 18 | 17 | 12 | 11 | 6 | 5 | 0 |
|----:|----:|----:|----:|----:|----:|----:|---:|---:|---:|
| 0 | 0 | 0 | 0 | 0x0000 | 0x0000 | 0x0000 |    |    |    |

cmd x represents pattern table entries. x here is the index, 0 ~ 3.

Figure 34.2-3. APB_SARADC_SAR_PATT_TAB1_REG and Pattern Table Entry 0 - Entry 3

(reserved)

| 31 | 24 | 23 | 18 | 17 | 12 | 11 | 6 | 5 | 0 |
|----:|----:|----:|----:|----:|----:|----:|---:|---:|---:|
| 0 | 0 | 0 | 0 | 0x0000 | 0x0000 | 0x0000 |    |    |    |

cmd x represents pattern table entries. x here is the index, 4 ~ 7.

Figure 34.2-4. APB_SARADC_SAR_PATT_TAB2_REG and Pattern Table Entry 4 - Entry 7

Each register consists of four 6-bit pattern table entries. Each entry is composed of three fields that contain working ADC, ADC channel and attenuation information, as shown in Table 34.2-5.

Figure 34.2-5. Pattern Table Entry

| 5 | 4 | 2 | 1 | 0 |
|---:|---:|---:|---:|---:|
| x | xx | x | x |

atten Attenuation. 0: 0 dB; 1: 2.5 dB; 2: 6 dB; 3: 12 dB.

ch_sel ADC channel, see Table 34.2-1.

sar_sel Working ADC. 0: SAR ARC1; 1: SAR ADC2.

Configuration of multi-channel scanning

In this example, two channels are selected for multi-channel scanning:

• Channel 2 of SAR ADC1, with the attenuation of 12 dB
```