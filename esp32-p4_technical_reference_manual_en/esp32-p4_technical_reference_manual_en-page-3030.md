

```markdown
Each pattern is 6 bits wide, consisting of two fields where conversion rules are stored. Figure 62.5-6 shows the pattern format and is followed by the descriptions of each field.

Figure 62.5-6. Pattern Structure

atten Configures attenuation:
0: 0 dB
1: 2.5 dB
2: 6 dB
3: 12 dB

ch_sel Configures channel. For HP ADC1, values 0-7 correspond to channels 0-7 individually, for HP ADC2, values 0-5 correspond to channels 0-5 individually.

## 62.5.7 HP ADC Pattern Configuration Example for Multi-channel Sampling

Assuming you want to implement the following sequence of HP ADC1 multi-channel sampling:

* Sample channel 2 of HP ADC1 with attenuation of 12 dB;
* Sample channel 0 of HP ADC1 with attenuation of 2.5 dB.

Then, the detailed configuration is as follows:

* Configure the first pattern (cmd0) of `ADC_SAR1_PATT_TAB1_REG[5:0]`:

Figure 62.5-7. cmd0 configuration

atten write 3 to this field, to set the attenuation to 12 dB.
ch_sel write 2 to this field, to select channel 2.

* Configure the second pattern (cmd1) of `ADC_SAR1_PATT_TAB1_REG[11:6]`:

Figure 62.5-8. cmd1 Configuration

atten write 1 to this field, to set the attenuation to 2.5 dB.
ch_sel write 0 to this field, to select channel 0.

* Configure `ADC_SAR1_PATT_LEN` to 1, i.e., set pattern table size to (this value + 1) = 2. Then patterns cmd0 and cmd1 will be used.
```