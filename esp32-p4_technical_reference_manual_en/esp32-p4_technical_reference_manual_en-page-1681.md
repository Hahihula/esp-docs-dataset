

```markdown
Register 36.18. ISP_LUT_CMD_REG (0x0048)

| Bit | Description         |
|-----|---------------------|
| 31  | (reserved)          |
| 17  | ISP_LUT_CMD          |
| 16  |                     |
| 15  |                     |
| 12  | ISP_LUT_NUM         |
| 11  |                     |
| 9   | ISP_LUT_ADDR        |
| 8   |                     |
| 0   | Reset               |

ISP_LUT_ADDR Configures the LUT address. When `ISP_LUT_NUM` selects LSC LUT, [11:10] being 0 indicates selecting Gb_B LUT, and being 1 indicates selecting R_Gr LUT. Bits [9:0] represent the actual LUT address.
(WT)

ISP_LUT_NUM Configures the LUT selection.
O: Select LSC LUT
Others: Invalid
(WT)

ISP_LUT_CMD Configures whether to read from or write to the LUT.
O: Read from the LUT
1: Write to the LUT
(WT)
```

```markdown
Register 36.19. ISP_LUT_WDATA_REG (0x004C)

| Bit | Description         |
|-----|---------------------|
| 31  |                     |
|     | 0x000000            |
| 0   | Reset               |

ISP_LUT_WDATA Data to be written to the LUT, which must be configured before writing to `ISP_LUT_CMD_REG`. (R/W)
```

```markdown
Register 36.20. ISP_LSC_TABLESIZE_REG (0x0054)

| Bit | Description         |
|-----|---------------------|
| 31  |                     |
|     | (reserved)          |
| 5   |                     |
| 4   |                     |
| 0   | Reset               |

ISP_LSC_XTABLESIZE Configures the number of horizontal grids in the LSC module. This value is obtained by `fix(((line_number - 1)/2/32) + 2`, where `fix()` denotes the rounding. (R/W)
```