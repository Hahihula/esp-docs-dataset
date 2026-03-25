

```markdown
Register 13.29. PMU_HP_SLEEP_HP_REGULATOR0_REG (0x0090)

| Bit | Description                  |
|-----|------------------------------|
| 31  | reserved                     |
| 19  | PMU_HP_SLEEP_HP_REGULATOR_XPD|
| 18  |                              |
| 17  |                              |
| ... | ...                          |
| 0   | Reset                        |

PMU_HP_SLEEP_HP_REGULATOR_XPD Configures whether to enable the HP sys regulator in
HP_SLEEP state.
O: Disable
1: Enable
(R/W)
```

```markdown
Register 13.30. PMU_HP_SLEEP_XTAL_REG (0x0098)

| Bit | Description                  |
|-----|------------------------------|
| 31  | reserved                     |
| 30  | PMU_HP_SLEEP_XPD_XTAL        |
| ... | ...                          |
| 0   | Reset                        |

PMU_HP_SLEEP_XPD_XTAL Configures whether to enable XTAL_CLK analog source in HP_SLEEP
state.
O: Disable
1: Enable
(R/W)
```