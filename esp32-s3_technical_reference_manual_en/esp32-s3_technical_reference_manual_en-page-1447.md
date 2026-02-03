**Title:**
Chapter 38 Pulse Count Controller (PCNT)

**Subtitle:**
38.5 Registers

**Body Text:**

The addresses in this section are relative to **Pulse Count Controller base address provided in Table 4.3-3 in Chapter 4 System and Memory**.

**Table Title:**
Register 38.1, PCNT_Un_CONF0_REG (n: 0-3) (0x000+0xC*n)

| Address | Description |
|---------|-------------|
| 0x0     | Reset       |
| 0x1     | PCNT_FILTER_THRESUn | This sets the maximum threshold, in APB_CLK cycles, for the filter. |
|         | Any pulses with width less than this will be ignored when the filter is enabled. (R/W) |
| 0x2     | PCNT_FILTER_ENUn | This is the enable bit for unit n’s input filter. (R/W) |
| 0x3     | PCNT_THR_ZERO_ENUn | This is the enable bit for unit n’s zero comparator. (R/W) |
|         |               | This is the enable bit for unit n’s thr_h_lim comparator. (R/W) |
| 0x4     | PCNT_THR_H_LIM_ENUn | This is the enable bit for unit n’s thr_h_lim comparator. (R/W) |
| 0x5     | PCNT_THR_L_LIM_ENUn | This is the enable bit for unit n’s thr_l_lim comparator. (R/W) |
|         |               | This is the enable bit for unit n’s thres0 comparator. (R/W) |
| 0x6     | PCNT_THRThRESO_ENUn | This is the enable bit for unit n’s thres0 comparator. (R/W) |
| 0x7     | PCNT_THRTHRESH1_ENUn | This is the enable bit for unit n’s thres1 comparator. (R/W) |
|         |               | This register sets the behavior when the signal input of channel O detects a negative edge. |
| 0x8     | PCNT_CHO_NEG_MODEUn | Increase the counter; 2: Decrease the counter; 0, 3: No effect on counter (R/W) |
|         |               | This register sets the behavior when the signal input of channel O detects a positive edge. |
|         |               | 1: Increase the counter; 2: Decrease the counter; 0, 3: No effect on counter (R/W) |
| 0x9     | PCNT_CHO_HCTRL_MODEUn | This register configures how the CHn_POS_MODE/CHn_NEG_MODE settings will be modified when the control signal is high. |
|         |               | O: No modification; 1: Invert behavior (increase → decrease, decrease → increase); 2, 3: Inhibit counter modification (R/W) |

**Footer Text:**
Continued on the next page...

**Page Footer Information:**
Espressif Systems
1447 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback