

```markdown
Register 16.54. TEE_CLOCK_GATE_REG (0x0080)

TEE_CLK_EN Configures whether to keep the clock always on.
O: enable automatic clock gating
1: keep the clock always on
(R/W)
```

```markdown
Register 16.55. TEE_DATE_REG (0x0FFC)

TEE_DATE_REG Version control register (R/W)
```

## 16.7.5 Low Power TEE Registers

```markdown
Register 16.56. LP_TEE_MO_MODE_CTRL_REG (0x0000)

LP_TEE_MO_MODE Configures MO security level mode.
0: tee_mode
1: ree_mode0
2: ree_mode1
3: ree_mode2
(R/W)
```

Espressif Systems

Submit Documentation Feedback

ESP32-C6 TRM (Version 1.1)
```