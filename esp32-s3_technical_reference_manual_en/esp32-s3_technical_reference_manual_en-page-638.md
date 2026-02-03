**Chapter Title:**
Chapter 11 System Timer (SYSTIMER)

**GoBack Link:** [GoBack](#)

---

### Section Header:
11.4.4 Interrupt

**Body Text:**
Each comparator has one level-triggered alarm interrupt, named as SYSTIMER_TARGETx_INT. Interrupt signal is asserted high when the comparator starts to alarm. Until the interrupt is cleared by software, it remains high.

To enable interrupts, set the bit SYSTIMER_TARGETx_INT_ENA.

---

### Section Header:
11.5 Programming Procedure

**Body Text:**
When configuring COMPx and UNITn, please ensure the corresponding COMP and UNIT are at work.

---

#### Subsection Title:
11.5.1 Read Current Count Value

**List of Steps:**
1. Set SYSTIMER_TIMER_UNITn_UPDATE to update the current count value into SYSTIMER_TIMER_UNITn_VALUE_HI and SYSTIMER_TIMER_UNITn_VALUE_LO.
2. Poll the reading of SYSTIMER_TIMER_UNITn_VALUE_VALID, till it's 1, which means user now can read the count values from SYSTIMER_TIMER_UNITn_VALUE_HI and SYSTIMER_TIMER_UNITn_VALUE_LO.
3. Read the low 32 bits and high 20 bits from SYSTIMER_TIMER_UNITn_VALUE_LO and SYSTIMER_TIMER_UNITn_VALUE_HI.

---

#### Subsection Title:
11.5.2 Configure One-Time Alarm in Target Mode

**List of Steps:**
1. Set SYSTIMER_TARGETx_TIMER_UNITn_SEL to select the counter (UNIT0 or UNIT1) used for COMPx.
2. Read current count value, see Section 11.5.1. This value will be used to calculate the alarm value (t) in Step 4.
3. Clear SYSTIMER_TARGETx_PERIOD_MODE to enable target mode.
4. Set an alarm value (t), and fill its low 32 bits to SYSTIMER_TIMER_TARGETx_LO, and the high 20 bits to SYSTIMER_TIMER_TARGETx_HI.
5. Set SYSTIMER_TIMER_COMPx_LOAD to synchronize the alarm value to COMPx, i.e., load the alarm value (t) to the COMPx.
6. Set SYSTIMER_TARGETx_WORK_EN to enable the selected COMPx. COMPx starts comparing the count value with the alarm value (t).
7. Set SYSTIMER_TARGETx_INT_ENA to enable timer interrupt. When Unitn counts to the alarm value (t), a SYSTIMER_TARGETx_INT is triggered.

---

**Footer:**
Espressif Systems
638 ESP32-S3 TRM (Version 1.7)

**Link:** [Submit Documentation Feedback](#)