Title: Chapter 38 Pulse Count Controller (PCNT)

Subtitle: GoBack

Section Title:
38.3.1 Channel O Incrementing Independently

Image Caption and Description:
Figure 38.3-1. Channel O Up Counting Diagram

Body Text:

Figure 38.3-1 illustrates how channel O is configured to increment independently on the positive edge of sig_ch0_un while channel 1 is disabled (see subsection **38.2** for how to disable channel 1). The configuration of channel O shown below.

- PCNT_CHO_LCTRL_MODE_Un=0: When ctrl_ch0_un is low, the counter mode specified for the low state turns on, in this case it is Increment mode.
- PCNT_CHO_HCTRL_MODE_Un=2: When ctrl_ch0_un is high, the counter mode specified for the low state turns on, in this case it is Disable mode.
- PCNT_CHO_POS_MODE_Un=1: The counter increments on the positive edge of sig_ch0_un.
- PCNT_CHO_NEG_MODE_Un=0: The counter idles on the negative edge of sig_ch0_un.
- PCNT_CNT_H_LIM_Un=5: When pulse_cnt counts up to PCNT_CNT_H_LIM_Un, it is cleared.

Section Title:
38.3.2 Channel O Decrementing Independently

Image Caption and Description:
Figure 38.3-2. Channel O Down Counting Diagram

Body Text:

Figure 38.3-2 illustrates how channel O is configured to decrement independently on the positive edge of sig_ch0_un while channel 1 is disabled. The configuration of channel O in this case differs from that in Figure 38.3-1 in the following aspects:
- PCNT_CHO_POS_MODE_Un=2: the counter decrements on the positive edge of sig_ch0_un.
- PCNT_CNT_L_LIM_Un=-5: when pulse_cnt counts down to PCNT_CNT_L_LIM_Un, it is cleared.

Footer Information:

Espressif Systems
1444 ESP32-S3 TRM (Version 1.7)

[Submit Documentation Feedback]