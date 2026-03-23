

```markdown
Chapter 39 On-Chip Sensor and Analog Signal Processing GoBack


Each register consists of four 6-bit pattern table entries. Each entry is composed of three fields that contain the ADC channel and attenuation information, as shown in Table 39.2-5.

Figure 39.2-5. Pattern Table Entry

```
| (reserved) | ch_sel | atten |
|:-----------:|:-------:|:------:|
|     5       |    4    |   2    |   1    |   0    |
|             O      | xx     | x      | x      |

```
atten Attenuation:
0: 0 dB
1: 2.5 dB
2: 6 dB
3: 12 dB

ch_sel ADC channel, see Table 39.2-1.

Configuration of multi-channel scanning

In this example, two channels are selected for multi-channel scanning:

* Channel 0 of SAR ADC, with the attenuation of 2.5 dB
* Channel 2 of SAR ADC, with the attenuation of 12 dB

The detailed configuration is as follows:

* Configure the first pattern table entry (cmd0):

Figure 39.2-6. cmd1 configuration

```
| (reserved) | ch_sel | atten |
|:-----------:|:-------:|:------:|
|     5       |    4    |   2    |   1    |   0    |
|             O      |        |   0    |   1    |

```
atten write the value of 1 to this field, to set the attenuation to 2.5 dB.
ch_sel write the value of 0 to this field, to select channel 0 (see Table 39.2-1).

* Configure the second pattern table entry (cmd1):

Figure 39.2-7. cmd0 Configuration

```
| (reserved) | ch_sel | atten |
|:-----------:|:-------:|:------:|
|     5       |    4    |   2    |   1    |   0    |
|             O      |        |   0    |   3    |

```
atten write the value of 3 to this field, to set the attenuation to 12 dB.
ch_sel write the value of 2 to this field, to select channel 2 (see Table 39.2-1).
```