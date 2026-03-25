

```markdown
36.3.2 Channel O Decrementing Independently

Figure 36.3-2 illustrates how channel 0 is configured to decrement independently on the positive edge of sig_ch0_un while channel 1 is disabled. The configuration of channel 0 in this case differs from that in Figure 36.3-1 in the following aspects:

*   PCNT_CHO_POS_MODE_Un=2: the counter decrements on the positive edge of sig_ch0_un.
*   PCNT_CNT_L_LIM_Un=-5: when pulse_cnt counts down to PCNT_CNT_L_LIM_Un, it is cleared.

36.3.3 Channel O and Channel 1 Incrementing Together

Figure 36.3-3 illustrates how channel 0 and channel 1 are configured to increment on the positive edge of sig_ch0_un and sig_ch1_un respectively at the same time. It can be seen in Figure 36.3-3 that control signal ctrl_ch0_un and ctrl_ch1_un have the same waveform, so as input pulse signal sig_ch0_un and sig_ch1_un. The configuration procedure is shown below.

*   For channel 0:

    *   PCNT_CHO_LCTRL_MODE_Un=0: When ctrl_ch0_un is low, the counter mode specified for the low state turns on, in this case it is Increment mode.
    *   PCNT_CHO_HCTRL_MODE_Un=2: When ctrl_ch0_un is high, the counter mode specified for the low state turns on, in this case it is Disable mode.
    *   PCNT_CHO_POS_MODE_Un=1: The counter increments on the positive edge of sig_ch0_un.
    *   PCNT_CHO_NEG_MODE_Un=0: The counter idles on the negative edge of sig_ch0_un.
```