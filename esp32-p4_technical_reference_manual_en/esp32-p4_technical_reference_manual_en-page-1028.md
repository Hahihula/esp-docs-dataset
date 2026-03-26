

```markdown
Register 14.29. PMU_IMM_SLEEP_SYSCLK_REG (0x00D0)

| 31 | 30 | 29 | 28 | 27 | ... | 0 |
|-----|----:|----:|----:|----:|-----|---|
| 0   | 0   | 0   | 0   | 0   | ... | 0 |

PMU_UPDATE_DIG_ICG_SWITCH Immediately updates function clock gating status. (WT)

PMU_TIE_LOW_ICG_SLP_SEL Configures whether to disable PMU control of function clock.
O: No effect
1: Disable
(WT)

PMU_TIE_HIGH_ICG_SLP_SEL Configures whether to enable PMU control of function clock.
O: No effect
1: Enable
(WT)

PMU_UPDATE_DIG_SYS_CLK_SEL Immediately updates system clock.
O: No effect
1: Updates the configurations of SYS_CLK_SEL in the current PMU state to the application side.
(WT)
```

Register 14.30. PMU_IMM_HP_FUNC_ICG_REG (0x00D4)

```markdown
| 31 | 30 |
|----|----|
| 0  | 0  |

PMU_UPDATE_DIG_ICG_FUNC_EN Immediately updates function clock gating bitmap. (WT)
```

Espressif Systems

Submit Documentation Feedback

ESP32-P4 TRM PRELIMINARY
```