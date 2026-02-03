**Chapter Title:**
Chapter 11 System Timer (SYSTIMER)

**Section Titles and Content:**

---

### **11.5.3 Configure Periodic Alarms in Period Mode**

- Set `SYSTIMER_TARGETx_TIMUNIT_SEL` to select the counter (UNIT0 or UNIT1) used for COMPx.
- Set a alarm period (δt), and fill it to `SYSTIMER_TARGETx_PERIOD`.
- Set `SYSTIMER_TIMER_COMPx_LOAD` to synchronize the alarm period (δt) to COMPx, i.e., load the alarm period (δt) to COMPx.
- Clear and then set `SYSTIMER_TARGETx_PERIOD_MODE` to configure COMPx into period mode.
- Set `SYSTIMER_TARGETx_WORK_EN` to enable the selected COMPx. COMPx starts comparing the count value with the sum of start value + n*δt (n = 1, 2, 3...).
- Set `SYSTIMER_TARGETx_INT_ENA` to enable timer interrupt. A SYSTIMER_TARGETx_INT interrupt is triggered when Unitn counts to start value + n*δt (n = 1, 2, 3...) set in step 2.

---

### **11.5.4 Update After Light-sleep**

- Configure the RTC timer before the chip goes to Light-sleep, to record the exact sleep time. For more information, see Chapter 10 Low-power Management (RTC_CNTL).
- Read the sleep time from the RTC timer when the chip is woken up from Light-sleep.
- Read current count value of system timer, see Section **11.5.1**.
- Convert the time value recorded by the RTC timer from the clock cycles based on RTC_SLOW_CLK to that based on 16 MHz CNTL_CLK. For example, if the frequency of RTC_SLOW_CLK is 32 KHz, the recorded the RTC timer value should be converted by multiplying by 500.
- Add the converted RTC value to current count value of system timer:
  - Fill the new value into `SYSTIMER_TIMER_UNITn_LOAD_LO` (low 32 bits) and `SYSTIMER_TIMER_UNITn_LOAD_HI` (high 20 bits).
  - Set `SYSTIMER_TARGETxUnitn_LOAD` to load new timer value into system timer. In such a way, the system timer is updated.

---

### **11.6 Register Summary**

The addresses in this section are relative to system timer base address provided in Table 4.3-3 in Chapter 4 System and Memory.
The abbreviations given in Column Access are explained in Section [Access Types for Registers](#).

**Table:**
| Name                   | Description                                                                                     | Address       | Access |
|------------------------|--------------------------------------------------------------------------------------------------|---------------|--------|
| Clock Control Register | Configures system timer clock                                                                  | 0x0000        | R/W    |
| UNIT0 Control and Configuration Registers | - `SYSTIMERUnit0_OP_REG`: Read UNITO value to registers<br>- `SYSTIMERUnit0_LOAD_HI_REG`: High 20 bits to be loaded to UNITO<br>- `SYSTIMERUnit0_LOAD_LO_REG`: Low 32 bits to be loaded to UNITO<br>- `SYSTIMERUnit0_VALUE_HI_REG`: UNITO value, high 20 bits | varies       | R/W    |

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback

---