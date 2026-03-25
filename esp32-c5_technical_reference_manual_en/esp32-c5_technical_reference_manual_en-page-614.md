

```markdown
Chapter 13 Low-Power Management

GoBack

*   PMU_MODEM_SWITCH_SLEEP_END_INT: Triggered when the PMU state has switched from HP_MODEM to HP_SLEEP.
*   PMU_SLEEP_SWITCH_MODEM_END_INT: Triggered when the PMU state has switched from HP_SLEEP to HP_MODEM.
*   PMU_SLEEP_SWITCH_ACTIVE_END_INT: Triggered when the PMU state has switched from HP_SLEEP to HP_ACTIVE.
*   PMU_MODEM_SWITCH_ACTIVE_END_INT: Triggered when the PMU state has switched from HP_MODEM to HP_ACTIVE.
*   PMU_LP_CPU_WAKEUP_INT: Triggered when LP CPU is woken up.

Each interrupt source can be configured by a common set of registers that are described in Section Interrupt Configuration Registers. The specific registers can be found in Section 13.9 Register Summary.
```