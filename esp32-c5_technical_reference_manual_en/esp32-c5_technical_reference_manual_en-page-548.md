

```markdown
Register 12.12. SOC_ETM_TASK_ST4_REG (0x01F0)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | (reserved) | SOC_ETM_LULP_TASK_START_ST | SOC_ETM_L2SO_TASK_WAKEUP_CPU_ST | SOC_ETM_L2SO_TASK_STOP_TX_ST | SOC_ETM_L2SO_TASK_STOP_RX_ST | SOC_ETM_TMPSNSR_TASK_START_TX_ST | SOC_ETM_TMPSNSR_TASK_STOP_SAMPLE_ST | (reserved) |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | Reset |
```

SOC_ETM_TMPSNSR_TASK_START_SAMPLE_ST Represents TMPSNSR_TASK_START_SAMPLE trigger status.
- O: Not triggered
- 1: Triggered (R/WTC/SS)

SOC_ETM_TMPSNSR_TASK_STOP_SAMPLE_ST Represents TMPSNSR_TASK_STOP_SAMPLE trigger status.
- O: Not triggered
- 1: Triggered (R/WTC/SS)

SOC_ETM_I2SO_TASK_START_RX_ST Represents I2SO_TASK_START_RX trigger status.
- O: Not triggered
- 1: Triggered (R/WTC/SS)

SOC_ETM_I2SO_TASK_START_TX_ST Represents I2SO_TASK_START_TX trigger status.
- O: Not triggered
- 1: Triggered (R/WTC/SS)

Continued on the next page...
```