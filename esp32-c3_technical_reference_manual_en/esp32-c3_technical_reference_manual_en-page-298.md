

```markdown
Register 11.10. TIMG_WDTCONFIG0_REG (0x0048)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 18 | 17 | 15 | 14 | 13 | 12 | 11 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    | TIMG_WDT_EN | TIMG_WDT_STGO | TIMG_WDT_STG1 | TIMG_WDT_STG2 | TIMG_WDT_STG3 | TIMG_WDT_CONF_UPDATE_EN | TIMG_WDT_USE_XTAL | TIMG_WDT_CPU_RESET_LENGTH | TIMG_WDT_SYS_RESET_LENGTH | TIMG_WDT_FLASHBOOT_MOD_EN | TIMG_WDT_APPCPU_RESET_EN | TIMG_WDT_PROCPU_RESET_EN | (reserved) |
|     |    |             |              |               |                |                 |                         |                      |                           |                          |                        |                       |                     |                  |
| Value | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0x01 | 0x01 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |

TIMG_WDT_APPCPU_RESET_EN WDT reset CPU enable. (R/W)
TIMG_WDT_PROCPU_RESET_EN WDT reset CPU enable. (R/W)
TIMG_WDT_FLASHBOOT_MOD_EN When set, Flash boot protection is enabled. (R/W)

TIMG_WDT_SYS_RESET_LENGTH System reset signal length selection. 0: 100 ns, 1: 200 ns, 2: 300 ns, 3: 400 ns, 4: 500 ns, 5: 800 ns, 6: 1.6 µs, 7: 3.2 µs. (R/W)

TIMG_WDT_CPU_RESET_LENGTH CPU reset signal length selection. 0: 100 ns, 1: 200 ns, 2: 300 ns, 3: 400 ns, 4: 500 ns, 5: 800 ns, 6: 1.6 µs, 7: 3.2 µs. (R/W)

TIMG_WDT_USE_XTAL Chooses WDT clock. 0: APB_CLK; 1:XTAL_CLK. (R/W)

TIMG_WDT_CONF_UPDATE_EN Updates the WDT configuration registers. (WT)

TIMG_WDT_STG3 Stage 3 configuration. 0: off, 1: interrupt, 2: reset CPU, 3: reset system. (R/W)

TIMG_WDT_STG2 Stage 2 configuration. 0: off, 1: interrupt, 2: reset CPU, 3: reset system. (R/W)

TIMG_WDT_STG1 Stage 1 configuration. 0: off, 1: interrupt, 2: reset CPU, 3: reset system. (R/W)

TIMG_WDT_STGO Stage 0 configuration. 0: off, 1: interrupt, 2: reset CPU, 3: reset system. (R/W)

TIMG_WDT_EN When set, MWDT is enabled. (R/W)


Register 11.11. TIMG_WDTCONFIG1_REG (0x004C)

| Bit | 31 | 16 | 15 |
|-----|----|----|----|
|     |    | 0x01 | 0 |
|     |    |      | Reset |

TIMG_WDT_DIVCNT_RST When set, WDT's clock divider counter will be reset. (WT)

TIMG_WDT_CLK_PRESCALE MWDT clock prescaler value. MWDT clock period = MWDT's clock source period * TIMG_WDT_CLK_PRESCALE. (R/W)
```