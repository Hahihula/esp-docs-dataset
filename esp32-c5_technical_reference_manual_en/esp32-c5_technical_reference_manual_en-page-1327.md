

```markdown
Chapter 36 Pulse Count Controller (PCNT)

GoBack


suitable for periodically monitoring whether the count has decreased by a specified multiple, facilitating quantitative sampling, data statistics, or regular event handling.

If PCNT_CNT_H_LIM_Un and/or PCNT_CNT_L_LIM_Un are reconfigured by software when PCNT is working, the new configuration will take effect after pluse_cnt counts to any of the above seven watchpoints; if PCNT_CNT_THRESO_Un, PCNT_CNT_THRES1_Un, PCNT_CNT_H_STEP_Un and/or PCNT_CNT_L_STEP_Un are reconfigured by software, the new configuration will take effect immediately.

36.3 Applications

In each unit, channel 0 and channel 1 can be configured to work independently or together. The three subsections below provide details of channel 0 incrementing independently, channel 0 decrementing independently, and channel 0 and channel 1 incrementing together. For other working modes not elaborated in this section (e.g. channel 1 incrementing/decrementing independently, or one channel incrementing while the other decrementing), reference can be made to these three subsections.

36.3.1 Channel 0 Incrementing Independently

Figure 36.3-1 illustrates how channel 0 is configured to increment independently on the positive edge of sig_chO_un while channel 1 is disabled (see subsection 36.2 for how to disable channel 1). The configuration of channel 0 is shown below.

*   PCNT_CHO_LCTRL_MODE_Un=0: When ctrl_chO_un is low, the counter mode specified for the low state turns on, in this case it is Increment mode.
*   PCNT_CHO_HCTRL_MODE_Un=2: When ctrl_chO_un is high, the counter mode specified for the low state turns on, in this case it is Disable mode.
*   PCNT_CHO_POS_MODE_Un=1: The counter increments on the positive edge of sig_chO_un.
*   PCNT_CHO_NEG_MODE_Un=0: The counter idles on the negative edge of sig_chO_un.
*   PCNT_CNT_H_LIM_Un=5: When pulse_cnt counts up to PCNT_CNT_H_LIM_Un, it is cleared.

Figure 36.3-1. Channel 0 Up Counting Diagram
```