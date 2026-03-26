

```markdown
Register 16.11. TIMG_WDTCONFIG1_REG (0x004C)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                 |                                                                             |
|     | TIMG_WDT_DIVCNT_RST            | Configures whether to reset WDT’s clock divider counter.                    |
|     |                                 | 0: No effect                                                                |
|     |                                 | 1: Reset (WT)                                                               |
| 16  | TIMG_WDT_CLK_PRESCALE           | Configures MWDT clock prescaler value. Valid only when write protection is disabled. |
|     |                                 | MWDT clock period = 12.5 ns *TIMG_WDT_CLK_PRESCALE. (R/W)                   |

Register 16.12. TIMG_WDTCONFIG2_REG (0x0050)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                 |                                                                             |
|     | TIMG_WDT_STGO_HOLD              | Configures the stage 0 timeout value. Valid only when write protection is disabled. |
|     |                                 | Measurement unit: mwdt_clk. (R/W)                                           |
```