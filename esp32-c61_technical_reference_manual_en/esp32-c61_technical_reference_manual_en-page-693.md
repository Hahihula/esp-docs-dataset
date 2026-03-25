

```markdown
Register 16.24. HP_APM_DATE_REG (0x07FC)

HP_APM_DATE Version control register. (R/W)


16.9.2 LP_APM_REG

The addresses in this section are relative to the LP_APM base address provided in Table 4.3-2 in Chapter 4 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.


Register 16.25. LP_APM_REGION_FILTER_EN_REG (0x0000)

LP_APM_REGION_FILTER_EN Configure bit n (0-3) to enable permission checks for region n (0-3).
O: Disable
1: Enable
(R/W)


Register 16.26. LP_APM_REGIONn_ADDR_START_REG (n: 0-3) (0x0004+0xC*n)

LP_APM_REGIONn_ADDR_START Configures the start address of region n. (R/W)
```