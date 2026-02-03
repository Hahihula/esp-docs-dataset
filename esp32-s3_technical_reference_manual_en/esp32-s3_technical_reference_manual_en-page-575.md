**Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Diagram and Caption for Figure 10.3-8: Brown-out detector**

```
VREF
    |
VDD3P3_RTC   VDD3P3_CPU   VDDA1   VDDA2
    |                   |
    +-------------------+
           comp

Figure 10.3-8. Brown-out detector
```

**Body Text:**
RTC_CNTL_RTC_BROWN_OUT_DET indicates the output level of brown-out detector. This register is low level by default, and outputs high level when the voltage of the detected pin drops below the predefined threshold.

When a brown-out signal is detected, the brownout detector can handle it in one of the two methods described below:

- **mode0:** triggers an interrupt when the counter counts to the thresholds pre-defined in int comparer and rst comparer, then resets the chip based on the rst_sel configuration. This method can be enabled by setting the bod_mode0_en signal.
  
- **mode1:** resets the system directly.

**Workflow is illustrated in the diagram below:**

```
bod_mode0_int
  |
  v
bod_mode0_en -> Int Comparer
  |               |
v  |              |
v  +-------------+
|               |
|   Rst         |
|  Comparator   |
+---------------+
       |
       v
bod_mode0_rst_sel -> Chip Reset

Brown-out Detected
  |
  v
bod_mode1_rst_en -> System Reset
```

**Diagram and Caption for Figure 10.3-9: Brown-out detector**

```
bod_mode1_rst_en | bod_mode1_sel
    +-----------+-------------+
           AND
    +-----------+
           |
           v
bod_mode1_rst_en
```

**Footer Text:**
Registers for controlling related signals are described below:

Espressif Systems

575 ESP32-S3 TRM (Version 1.7)

Submit Documentation Feedback