

```markdown
Register 18.26. HP_APM_INT_EN_REG (0x0118)

31 | 5 | 4 | 3 | 2 | 1 | 0
--+-----+-----+-----+-----+-----+-----
| Reset | reserved |

HP_APM_MO_APM_INT_EN Configures to enable HP_APM_CTRL MO interrupt.
O: Disable
1: Enable
(R/W)

HP_APM_M1_APM_INT_EN Configures to enable HP_APM_CTRL M1 interrupt.
O: Disable
1: Enable
(R/W)

HP_APM_M2_APM_INT_EN Configures to enable HP_APM_CTRL M2 interrupt.
O: Disable
1: Enable
(R/W)

HP_APM_M3_APM_INT_EN Configures to enable HP_APM_CTRL M3 interrupt.
O: Disable
1: Enable
(R/W)

HP_APM_M4_APM_INT_EN Configures to enable HP_APM_CTRL M4 interrupt.
O: Disable
1: Enable
(R/W)
```

```markdown
Register 18.27. HP_APM_CLOCK_GATE_REG (0x07F8)

31 | 1 | 0
--+-----+-----
| Reset | reserved |

HP_APM_CLK_EN Configures whether to keep the clock always on.
O: Enable automatic clock gating
1: Keep the clock always on
(R/W)
```