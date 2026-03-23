
```markdown
Register 14.74. SYSCON_FLASH_ACEn_ATTR_REG (n: 0 - 3) (0x0028 + 4*n)

| Bit 31 | ... | 9 | 8 | 7 | ... | 0 |
|--------|-----|---|---|---|-----|---|
|        |     |   |   |   |     | Reset |
| O      | xff |   |   |   |     |       |

SYSCON_FLASH_ACEn_ATTR Configures the permission to Region n of Flash. (R/W)

Register 14.75. SYSCON_FLASH_ACEn_ADDR_REG (n: 0-3) (0x0038 + 4*n)

| Bit 31 | ... | 0 |
|--------|-----|---|
|        |     | Reset |
| 0x000000 |       |

SYSCON_FLASH_ACEn_ADDR_S Configure the starting address of Flash Region n. The size of each region should be aligned to 64 KB. (R/W)
```