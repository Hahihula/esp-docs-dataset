

```markdown
| Internal Interrupt Source                     | Trigger Condition                                      | Interrupt Signal |
|-----------------------------------------------|--------------------------------------------------------|------------------|
| PCNT_CNT_THR_EVENT_UO_INT                     | reaching the watchpoint in PCNT unit 0                 | PCNT_INT         |
| PCNT_CNT_THR_EVENT_U1_INT                     | reaching the watchpoint in PCNT unit 1                 | PCNT_INT         |
| PCNT_CNT_THR_EVENT_U2_INT                     | reaching the watchpoint in PCNT unit 2                 | PCNT_INT         |
| PCNT_CNT_THR_EVENT_U3_INT                     | reaching the watchpoint in PCNT unit 3                 | PCNT_INT         |

Note:
For definitions of interrupt, interrupt signal, interrupt source, and their correlations, please refer to Chapter 12 Interrupt Matrix > Section 12.2 Interrupt Terminology in ESP32-P4.
```

## 48.6 Programming Procedures

In each unit, channel 0 and channel 1 can be configured to work independently or together. The three subsections below provide details of channel 0 incrementing independently, channel 0 decrementing independently, and channel 0 and channel 1 incrementing together. For other working modes not elaborated in this section (e.g., channel 1 incrementing/decrementing independently, or one channel incrementing while the other decrementing), reference can be made to these three subsections.

### 48.6.1 Channel 0 Incrementing Independently

![Figure 48.6-1. Channel 0 Up Counting Diagram](#)

Figure 48.6-1 illustrates how channel 0 is configured to increment independently on the rising edge of sig_chO_un while channel 1 is disabled (see Subsection 48.4 for how to disable channel 1). The configuration of channel 0 is shown below.

*   `PCNT_CHO_LCTRL_MODE_Un=0`: When ctrl_chO_un is low, the counter mode specified for the low state turns on, in this case it is Increment mode.
*   `PCNT_CHO_HCTRL_MODE_Un=2`: When ctrl_chO_un is high, the counter mode specified for the low state turns on, in this case it is Disable mode.
*   `PCNT_CHO_POS_MODE_Un=1`: The counter increments on the rising edge of sig_chO_un.
```