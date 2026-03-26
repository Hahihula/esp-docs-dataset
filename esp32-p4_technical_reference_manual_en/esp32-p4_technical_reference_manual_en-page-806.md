

```markdown
Register 12.134. COREO_CLOCK_GATE_REG (0x0210)

COREO_REG_CLK_EN Configures whether to force interrupt register clock-gate on.
- O: No effect
- 1: Force interrupt register clock-gate on
(R/W)
```

```markdown
Register 12.135. COREO_INTR_STATUS_REG_4_REG (0x0220)

COREO_INTR_STATUS_4 Represents the status of the interrupt sources from 128 ~ 130. Each bit corresponds to one interrupt source. (RO)
```

```markdown
Register 12.136. COREO_INTR_SIG_IDX_ASSERT_IN_SEC_REG (0x0228)

COREO_INTR_SIG_IDX_ASSERT_IN_SEC Configures which peripheral machine mode interrupt of CPU0 is used as the target for the interrupt delegation function. Valid values range from 16 ~ 47.
(R/W)
```