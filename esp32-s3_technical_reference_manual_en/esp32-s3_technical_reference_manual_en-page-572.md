**Chapter Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Section Header:**
ULP Coprocessor (ULP-FSM, ULP-RISC-V). For detailed description of touch timer, please refer to Chapters 39 On-Chip Sensors and Analog Signal Processing.

**Body Text:**
The readable 48-bit RTC timer is a real-time counter (using RTC slow clock) that can be configured to log the time when one of the following events happens. For details, see Table 10.3-2.

**Table Title:**
Table 10.3-2. The Triggering Conditions for the RTC Timer

| Enabling Options | Triggering Conditions |
| --- | --- |
| RTC_CNTL_TIMER_XTL_OFF | RTC main state machine powers down or XTAL_CLK crystal powers up. |
| RTC_CNTL_TIMER_SYSSTALL | CPU enters or exits the stall state. This is to ensure the SYS_TIMER is continuous in time. |
| RTC_CNTL_TIMERSYS_RST | Resetting digital core completes. |
| RTC_REG_TIME_UPDATE | Register RTC_CNTL_RTC_TIME_UPDATE is configured by CPU (i.e., users). |

**Body Text:**
The RTC timer updates two groups of registers upon any new trigger. The first group logs the time of the current trigger, and the other logs the previous trigger. Detailed information about these two register groups is shown below:

- **Register group 0:** logs the status of RTC timer at the current trigger.
  - RTC_CNTL_RTC_TIME_HIGH0_REG
  - RTC_CNTL_RTC_TIME_LOW0_REG

- **Register group 1:** logs the status of RTC timer at the previous trigger.
  - RTC_CNTL_RTC_TIME_HIGH1_REG
  - RTC_CNTL_RTC_TIME_LOW1_REG

On a new trigger, information on previous trigger is moved from register group 0 to register group 1 (and the original trigger logged in register group 1 is overwritten), and this new trigger is logged in register group 0. Therefore, only the last two triggers can be logged at any time.

It should be noted that any reset/sleep other than power-up reset will not stop or reset the RTC timer.
Also, the RTC timer can be used as a wakeup source. For details, see Section 10.4.4.

**Subsection Title:**
10.3.4 Voltage Regulators

**Body Text:**
ESP32-S3 has three voltage regulators to regulate the power supply to different power domains:

- Digital voltage regulator for digital power domains;
- Low-power voltage regulator for RTC power domains;
- Flash voltage regulator for the rest of power domains.

**Note:**
For a full list of power domains, please refer to Section 10.4.1

**Footer Information:**
Espressif Systems
Page number: 572
Document version and type: ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback