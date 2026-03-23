

```markdown
Register 16.22. SYSCON_MEM_POWER_DOWN_REG (0x00A8)

| Bit | Field Name                     |
|-----|--------------------------------|
| 31  | (reserved)                    |
| 6   | SYSCON_SRAM_POWER_DOWN        |
| 5   | SYSCON_ROM_POWER_DOWN         |
| 2-1 | Reset                         |
| 0   |                                |

SYSCON_ROM_POWER_DOWN    Set this field to send the internal ROM into retention state. (R/W)
SYSCON_SRAM_POWER_DOWN   Set this field to send the internal SRAM into retention state. (R/W)

Register 16.23. SYSCON_MEM_POWER_UP_REG (0x00AC)

| Bit | Field Name                     |
|-----|--------------------------------|
| 31  | (reserved)                    |
| 6   | SYSCON_SRAM_POWER_UP          |
| 5   | SYSCON_ROM_POWER_UP           |
| 2-1 | Reset                         |
| 0   |                                |

SYSCON_ROM_POWER_UP       Set this field to force the internal ROM to work as normal (do not enter the retention state) when the chip enters light sleep. (R/W)
SYSCON_SRAM_POWER_UP      Set this field to force the internal SRAM to work as normal (do not enter the retention state) when the chip enters light sleep. (R/W)
```