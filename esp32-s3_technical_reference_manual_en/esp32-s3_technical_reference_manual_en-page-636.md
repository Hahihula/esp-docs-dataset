**Chapter Title:**
Chapter 11 System Timer (SYSTIMER)

**Section Header:**
GoBack

**Body Text with Code and Descriptions:**

- SYSTIMER_TIMER UNITn WORK_EN:
  - Description: set this bit to enable the counter UNITn in system timer.

- SYSTIMER_TIMER UNITn CORE0_STALL_EN:
  - Description: if this bit is set, the counter UNITn stops counting when CPU0 is stalled. The counter continues its counting after the CPU0 resumes.
  
- SYSTIMER_TIMER UNITn CORE1_STALL_EN:
  - Description: if this bit is set, the counter UNITn stops counting when CPU1 is stalled. The counter continues its counting after the CPU1 resumes.

**Explanation of Configuration Bits for Counter:**
The configuration of three bits to control the counter UNITn as shown below:

| SYSTIMER_TIMER UNITn WORK_EN | SYSTIMER_TIMER UNITn CORE0_STALL_EN | SYSTIMER_TIMER UNITn CORE1_STALL_EN | Counter |
|-------------------------------|---------------------------------------|--------------------------------------|---------|
| 0                             | x                                     | x                                    | Not at work |
| 1                             | x                                     | 1                                    | Stop counting, but will continue its counting after CPU1 resumes. |
| 1                             | 1                                     | x                                    | Stop counting, but will continue its counting after CPU0 resumes. |
| 1                             | 0                                     | 0                                    | Keep counting |

**Note:**
*x: Don't-care.*

When the counter UNITn is at work, the count value is incremented on each counting cycle.

The low 32 bits and high 20 bits of initial count value are loaded from SYSTIMER_TIMER UNITn LOAD_LO and SYSTIMER_TIMER UNITn LOAD_HI. Writing to a bit in SYSTIMER_TIMER UNITn LOAD triggers a reload event, and the current count value will be changed immediately. If UNITn is at work, the counter will continue to count up from the new reload value.

Writing 1 to SYSTIMER_TIMER UNITn UPDATE will trigger an update event. The low 32 bits and high 20 bits of current count value will be locked into SYSTIMER_TIMER UNITn VALUE_LO and SYSTIMER_TIMER UNITn VALUE_HI, then SYSTIMER_TIMER UNITn VALUE_VALID is asserted.

**Section Header:**
11.4.2 Comparator and Alarm

**Body Text with Configuration Details for Comparators (COMPx):**

The system timer has three 52-bit comparators shown as COMPx (x = 0, 1, or 2). The comparators can generate independent interrupts based on different alarm values (t) or alarm periods (δt).

Configure SYSTIMER_TARGETx PERIODx_MODE to choose from the two alarm modes for each COMPx:

- 1: select period mode
- 0: select target mode

In period mode, the alarm period (δt) is provided by the register SYSTIMER_TARGETx PERIOD. Assuming that current count value is t1 when it reaches (t1 + δt), an alarm interrupt will be generated.

**Footer Information:**
Espressif Systems
636 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback