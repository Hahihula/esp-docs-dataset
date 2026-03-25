

```markdown
## 18.9.3 LP_APMO_REG

The addresses in this section are relative to the LP_APMO base address provided in Table 6.3-2 in Chapter 6 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

### Register 18.45. LP_APMO_REGION_FILTER_EN_REG (0x0000)

LP_APMO_REGION_FILTER_EN Configures bit n (0-7) to enable permission checks for region n (0-7).
*   O: Disable
*   1: Enable
(R/W)
```

```markdown
### Register 18.46. LP_APMO_REGIONn_ADDR_START_REG (n: 0-7) (0x0004+0xC*n)

LP_APMO_REGIONn_ADDR_START Configures the start address of region n. (R/W)
```