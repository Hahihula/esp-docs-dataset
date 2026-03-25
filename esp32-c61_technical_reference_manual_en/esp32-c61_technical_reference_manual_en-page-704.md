

```markdown
Register 16.50. CPU_APM_INT_EN_REG (0x0118)

CPU_APM_MO_APM_INT_EN   Configures whether to enable CPU_APM_CTRL MO interrupt.
    0: Disable
    1: Enable
    (R/W)

CPU_APM_MI_APM_INT_EN   Configures whether to enable CPU_APM_CTRL MI interrupt.
    0: Disable
    1: Enable
    (R/W)
```

```markdown
Register 16.51. CPU_APM_CLOCK_GATE_REG (0x07F8)

CPU_APM_CLK_EN   Configures whether to keep the clock always on.
    0: Enable automatic clock gating
    1: Keep the clock always on
    (R/W)
```

```markdown
Register 16.52. CPU_APM_DATE_REG (0x07FC)

CPU_APM_DATE   Version control register. (R/W)
```