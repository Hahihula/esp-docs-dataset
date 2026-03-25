

```markdown
Register 11.28. PMU_SLP_WAKEUP_CNTLO_REG (0x0120)

PMU_SLEEP_REQ Configures whether to switch the chip’s PMU state to HP_SLEEP or LP_SLEEP.
O: Do not switch
1: Switch to HP_SLEEP or LP_SLEEP, depending on the state of the LP CPU.
(WT)

Register 11.29. PMU_SLP_WAKEUP_CNTLI_REG (0x0124)

PMU_SLEEP_REJECT_ENA Configures the sleep rejection source. For the mapping between values and sources please refer to Table 11.4-1. (R/W)

PMU_SLP_REJECT_EN Configures whether to enable sleep rejection function.
O: Disable
1: Enable
(R/W)

Register 11.30. PMU_SLP_WAKEUP_CNTL2_REG (0x0128)

PMU_WAKEUP_ENA Configures wake-up source. For the mapping between values and sources please refer to Table 11.4-1. (R/W)
```