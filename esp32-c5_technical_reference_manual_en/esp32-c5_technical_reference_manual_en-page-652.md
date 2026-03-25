

```markdown
Register 13.49. PMU_HP_INT_CLR_REG (0x016C)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | ... | 0 |
|-----|----|----|----|----|----|----|-----|---|
|     | 0  | 0  | 0  | 0  | 0  | 0  | ... | 0 |
| Reset |    |    |    |    |    |    |     |   |

PMU_LP_CPU_EXC_INT_CLR Write 1 to clear PMU_LP_CPU_EXC_INT. (WT)
PMU_SDIO_IDLE_INT_CLR Write 1 to clear PMU_SDIO_IDLE_INT. (WT)
PMU_SW_INT_CLR Write 1 to clear PMU_SW_INT. (WT)
PMU_SOC_SLEEP_REJECT_INT_CLR Write 1 to clear PMU_SOC_SLEEP_REJECT_INT. (WT)
PMU_SOC_WAKEUP_INT_CLR Write 1 to clear PMU_SOC_WAKEUP_INT. (WT)
```