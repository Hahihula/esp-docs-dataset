

```markdown
Register 37.20. PPA_SRM_MEM_PD_REG (0x0068)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 3   | 2   | 1   | 0    |
| O   | O   | O   | O    |
| Reset| O   | O   | O    |

PPA_SRM_MEM_CLK_ENA Configures whether to enable the force enable of the SRM MEM clock.
- 0: Disable
- 1: Enable
(R/W)

PPA_SRM_MEM_FORCE_PD Configures whether to enable the force power down of SRM MEM.
- 0: Disable
- 1: Enable
(R/W)

PPA_SRM_MEM_FORCE_PU Configures whether to enable the force power up of SRM MEM.
- 0: Disable
- 1: Enable
(R/W)
```

```markdown
Register 37.21. PPA_REG_CONF_REG (0x006C)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
|     | PPACLK_EN (bit 1)                                                            |
| O   | O   | O   | O    |
| Reset| O   | O   | O    |

PPA_CLK_EN Configures whether to keep the PPA register clock always on.
- 0: Clock only turns on when there's a register access
- 1: Clock always on
(R/W)
```