

```markdown
Chapter 11 Low-Power Management

Register 11.52. PMU_IMM_HP_FUNC_ICG_REG (0x00D4)

PMU_UPDATE_DIG_ICG_FUNC_EN

31 30
+-----------------------------------------------+
| 0 | 0 | ... | 0 |
+-----------------------------------------------+
Reset

PMU_UPDATE_DIG_ICG_FUNC_EN Configure whether to force the PMU to update its ICG enable signals of HP system peripherals' function clocks based on the current PMU state.
O: No effect
1: Force update
(WT)

Register 11.53. PMU_IMM_HP_APB_ICG_REG (0x00D8)

PMU_UPDATE_DIG_ICG_APB_EN

31 30
+-----------------------------------------------+
| 0 | 0 | ... | 0 |
+-----------------------------------------------+
Reset

PMU_UPDATE_DIG_ICG_APB_EN Configure whether to force the PMU to update its ICG enable signals of HP system peripherals' APB clock based on the current PMU state.
O: No effect
1: Force update
(WT)
```