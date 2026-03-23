

```markdown
Chapter 16 Permission Control (PMS)

Register 16.51. LP_APMO_CLOCK_GATE_REG (0x00DC)
```

| Bit | Description |
|-----|-------------|
|     | (reserved)                     |
| 31  | LP_APMO_CLK_EN                 |

LP_APMO_CLK_EN Configures whether to keep the clock always on.
- O: enable automatic clock gating
- 1: keep the clock always on
(R/W)

Register 16.52. LP_APMO_DATE_REG (0x07FC)
```

| Bit | Description |
|-----|-------------|
| 31  | (reserved)                     |
| 28  | LP_APMO_DATE                   |

LP_APMO_DATE Version control register (R/W)

---

## 16.7.4 High Performance TEE Registers

Register 16.53. TEE_Mn_MODE_CTRL_REG (n: 0-31) (0x0000+0x4*n)
```

| Bit | Description |
|-----|-------------|
|     | (reserved)                     |
| 31  | TEE_Mn_MODE                   |

TEE_Mn_MODE Configures Mn security level mode.
- O: tee_mode
- 1: ree_mode0
- 2: ree_mode1
- 3: ree_mode2
(R/W)
```