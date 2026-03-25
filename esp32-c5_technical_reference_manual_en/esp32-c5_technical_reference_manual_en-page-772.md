

```markdown
Chapter 18 Permission Control (PMS)

Register 18.28. HP_APM_DATE_REG (0x07FC)
```

| 31 | 28 | 27 | ... | 0 |
|-----|----|----|-----|---|
| O   | O  | O  | Ox2312010 | Reset |

HP_APM_DATE Version control register. (R/W)

## 18.9.2 LP_APM_REG

The addresses in this section are relative to the LP_APM base address provided in Table 6.3-2 in Chapter 6 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

Register 18.29. LP_APM_REGION_FILTER_EN_REG (0x0000)

| 31 | ... | 7 | ... | 0 |
|----|-----|---|-----|---|
| O  | Ox1 |   |     | Reset |

LP_APM_REGION_FILTER_EN Configures bit n (0-7) to enable permission checks for region n (0-7).
*   0: Disable
*   1: Enable
(R/W)

Register 18.30. LP_APM_REGIONn_ADDR_START_REG (n: 0-7) (0x0004+0xC*n)

| 31 | ... | 0 |
|----|-----|---|
|    |     | Reset |

LP_APM_REGIONn_ADDR_START Configures the start address of region n. (R/W)
```