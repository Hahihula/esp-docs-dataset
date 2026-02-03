**Title: Chapter 11 System Timer (SYSTIMER)**

**Body Text:**
also will be generated when the count value reaches (t1 + 2*δt). By such way, periodic alarms are generated.

In target mode, the low 32 bits and high 20 bits of the alarm value (t) are provided by SYSTIMER_TIMER_TARGETx_LO and SYSTIMER_TIMER_TARGETx_HI. Assuming that current count value is t2 (t2 <= t), an alarm interrupt will be generated when the count value reaches the alarm value (t). Unlike in period mode, only one alarm interrupt is generated in target mode.

SYSTIMER_TARGETx_TIMER_UNSEL is used to choose the count value from which timer counter to be compared for alarm:

- 1: use the count value from UNIT0
- 0: use the count value from UNIT1

Finally, set SYSTIMER_TARGETx_WORK_EN and COMPx starts to compare the count value with the alarm value (t) in target mode or with the alarm period (t1 + n*δt) in period mode.

An alarm is generated when the count value equals to the alarm value (t) in target mode or to the start value (t1) + n*alarm period δt (n = 1,2,3...) in period mode. But if the alarm value (t) set in registers is less than current count value, i.e., the target has already passed, or current count value is larger than the real target value within a range (0 ~ 2^51 -1), an alarm interrupt also is generated immediately. The relationship between current count value t_c and alarm trigger point is shown below.

No matter in target mode or period mode, the low 32 bits and high 20 bits of the real target value can always be read from SYSTIMER_TARGETx_LO_RO and SYSTIMER_TARGETx_HI_RO.

**Table:**
- **Title:** Table 11.4-2. Trigger Point
- **Columns:** Relationship between t_c and t_t, Trigger Point

| t_c - t_t <= 0 | t_c = t_t, an alarm is triggered |
|----------------|----------------------------------|
| 0 <= t_c - t_t < 2^51 - 1 | An alarm is triggered immediately. |
| (t_c < 2^51 and t_t < 2^51) or t_c >= 2^51 and t_t > 2^51) | t_c overflows after counting to its maximum value 52^hffffff, and then starts counting up from 0. When its value reaches t_t, an alarm is triggered. |

**Subsection:**
- **Title:** Synchronization Operation

The clock APB_CLK is used in software operation, while timer counters and comparators are working on CNT_CLK. Synchronization is needed for some configuration registers. A complete synchronization action takes two steps:

1. Software writes suitable values to configuration fields, see the first column in Table 11.4-3.
2. Software writes 1 to corresponding bits to start synchronization, see the second column in Table 11.4-3.

**Table:**
- **Title:** Table 11.4-3. Synchronization Operation
- **Columns:** Configuration Fields, Synchronization Enable Bit

| [Configuration Fields] | [Synchronization Enable Bit] |
|--------------------------|-------------------------------|
|                           |                              |

**Footer Information:**
Espressif Systems  
637  
ESP32-S3 TRM (Version 1.7)  

[Submit Documentation Feedback](#)