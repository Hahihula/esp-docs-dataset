

```markdown
Register 13.47. PMU_HP_INT_ST_REG (0x0164)

| 31 | 30 | 29 | 28 | 27 | 26 | ... | ... | ... | ... | ... | Reset |
|-----|----|----|----|----|----|-----|-----|-----|-----|-----|-------|
| 0  | 0  | 0  | 0  | 0  | 0  | 0   | 0   | 0   | 0   | 0   | 0     |

PMU_LP_CPU_EXC_INT_ST The masked interrupt status of PMU_LP_CPU_EXC_INT. (RO)
PMU_SDIO_IDLE_INT_ST The masked interrupt status of PMU_SDIO_IDLE_INT. (RO)
PMU_SW_INT_ST The masked interrupt status of PMU_SW_INT. (RO)
PMU_SOC_SLEEP_REJECT_INT_ST The masked interrupt status of PMU_SOC_SLEEP_REJECT_INT. (RO)
PMU_SOC_WAKEUP_INT_ST The masked interrupt status of PMU_SOC_WAKEUP_INT. (RO)

Register 13.48. PMU_HP_INT_ENA_REG (0x0168)

| 31 | 30 | 29 | 28 | 27 | 26 | ... | ... | ... | ... | ... | Reset |
|-----|----|----|----|----|----|-----|-----|-----|-----|-----|-------|
| 0  | 0  | 0  | 0  | 0  | 0  | 0   | 0   | 0   | 0   | 0   | 0     |

PMU_LP_CPU_EXC_INT_ENA Write 1 to enable PMU_LP_CPU_EXC_INT. (R/W)
PMU_SDIO_IDLE_INT_ENA Write 1 to enable PMU_SDIO_IDLE_INT. (R/W)
PMU_SW_INT_ENA Write 1 to enable PMU_SW_INT. (R/W)
PMU_SOC_SLEEP_REJECT_INT_ENA Write 1 to enable PMU_SOC_SLEEP_REJECT_INT. (R/W)
PMU_SOC_WAKEUP_INT_ENA Write 1 to enable PMU_SOC_WAKEUP_INT. (R/W)
```