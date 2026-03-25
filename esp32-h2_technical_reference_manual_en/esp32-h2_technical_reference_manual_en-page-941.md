

```markdown
Chapter 32 Pulse Count Controller (PCNT) GoBack


32.3.3 Channel O and Channel 1 Incrementing Together

Figure 32.3-3 illustrates how channel 0 and channel 1 are configured to increment on the positive edge of sig_ch0_un and sig_ch1_un respectively at the same time. It can be seen in Figure 32.3-3 that control signal ctrl_ch0_un and ctrl_ch1_un have the same waveform, so as input pulse signal sig_ch0_un and sig_ch1_un. The configuration procedure is shown below.

• For channel 0:
    - PCNT_CHO_LCTRL_MODE_Un=0: When ctrl_ch0_un is low, the counter mode specified for the low state turns on, in this case it is Increment mode.
    - PCNT_CHO_HCTRL_MODE_Un=2: When ctrl_ch0_un is high, the counter mode specified for the low state turns on, in this case it is Disable mode.
    - PCNT_CHO_POS_MODE_Un=1: The counter increments on the positive edge of sig_ch0_un.
    - PCNT_CHO_NEG_MODE_Un=0: The counter idles on the negative edge of sig_ch0_un.

• For channel 1:
    - PCNT_CH1_LCTRL_MODE_Un=0: When ctrl_ch1_un is low, the counter mode specified for the low state turns on, in this case it is Increment mode.
    - PCNT_CH1_HCTRL_MODE_Un=2: When ctrl_ch1_un is high, the counter mode specified for the low state turns on, in this case it is Disable mode.
    - PCNT_CH1_POS_MODE_Un=1: The counter increments on the positive edge of sig_ch1_un.
    - PCNT_CH1_NEG_MODE_Un=0: The counter idles on the negative edge of sig_ch1_un.

• PCNT_CNT_H_LIM_Un=10: When pulse_cnt counts up to PCNT_CNT_H_LIM_Un, it is cleared.
```