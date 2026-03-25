

```markdown
Register 18.54. LP_APMO_INT_EN_REG (0x00D8)

LP_APMO_MO_APM_INT_EN Configures to enable LP_APMO_CTRL MO interrupt.
- O: Disable
- 1: Enable
(R/W)
```

```markdown
Register 18.55. LP_APMO_CLOCK_GATE_REG (0x00DC)

LP_APMO_CLK_EN Configures whether to keep the clock always on.
- O: Enable automatic clock gating
- 1: Keep the clock always on
(R/W)
```

```markdown
Register 18.56. LP_APMO_DATE_REG (0x07FC)

LP_APMO_DATE Version control register. (R/W)
```

## 18.9.4 CPU_APM_REG

The addresses in this section are relative to the CPU_APM base address provided in Table 6.3-2 in Chapter 6 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.
```