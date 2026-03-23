

```markdown
# 24.5 Register Summary

The addresses in this section are relative to Digital Signature base address provided in Table 5.3-2 in Chapter 5 *System and Memory*.

The abbreviations given in Column **Access** are explained in Section *Access Types for Registers*.

| Name                        | Description                          | Address | Access |
|-----------------------------|--------------------------------------|---------|--------|
| Configuration Registers     |                                      |         |        |
| DS_IV_O_REG                 | IV block data                        | 0x0630  | WO     |
| DS_IV_1_REG                 | IV block data                        | 0x0634  | WO     |
| DS_IV_2_REG                 | IV block data                        | 0x0638  | WO     |
| DS_IV_3_REG                 | IV block data                        | 0x063C  | WO     |
| Status/Control Registers    |                                      |         |        |
| DS_SET_START_REG            | Activates the DS module              | 0x0E00  | WO     |
| DS_SET_ME_REG               | Starts DS operation                  | 0x0E04  | WO     |
| DS_SET_FINISH_REG           | Ends DS operation                    | 0x0E08  | WO     |
| DS_QUERY_BUSY_REG           | Status of the DS module              | 0x0EOC  | RO     |
| DS_QUERY_KEY_WRONG_REG      | Checks the reason why `DS_KEY` is not ready | 0x0E10  | RO     |
| DS_QUERY_CHECK_REG          | Queries DS check result               | 0x0E14  | RO     |
| Version control register    |                                      |         |        |
| DS_DATE_REG                 | Version control register             | 0x0E20  | W/R    |
```