

```markdown
- PMU_MODEM_SWITCH_ACTIVE_END_INT: Triggered when the PMU state has switched from HP_MODEM to HP_ACTIVE.
- PMU_LP_CPU_WAKEUP_INT: Triggered when LP CPU is woken up.

LP_RTC_TIMER_INTR:

- RTC_TIMER_MAIN_TIMER_INT: Triggered when the count value of the RTC timer reaches the target value `RTC_TIMER_MAIN_TIMER_TAR_LOW0` or `RTC_TIMER_MAIN_TIMER_TAR_HIGH0`.

- RTC_TIMER_MAIN_TIMER_OVERFLOW_INT: Triggered when the count value of the RTC timer reaches the maximum value.
  ```
  MAX = (RTC_TIMER_MAIN_TIMER_TAR_HIGH0 << 32) + RTC_TIMER_MAIN_TIMER_TAR_LOW0
  ```

- LP_ANA_BOD_MODEO_INT: Triggered when the brownout detector detects that the voltage is below the threshold.

LP_RTC_TIMER_LP_INT:

- RTC_TIMER_MAIN_TIMER_LP_INT: Triggered when the count value of the RTC timer reaches the target value `RTC_TIMER_MAIN_TIMER_TAR_LOW1` or `RTC_TIMER_MAIN_TIMER_TAR_HIGH1`.

- RTC_TIMER_MAIN_TIMER_OVERFLOW_LP_INT: Triggered when the count value of the RTC timer reaches the maximum value.
  ```
  MAX = (RTC_TIMER_MAIN_TIMER_TAR_HIGH1 << 32) + RTC_TIMER_MAIN_TIMER_TAR_LOW1
  ```

- LP_ANA_BOD_MODEO_LP_INT: Triggered when the brownout detector detects that the voltage is below the threshold.

Each interrupt source can be configured by a common set of registers that are described in Section Interrupt Configuration Registers. The specific registers can be found in Section 12.9 Register Summary.
```