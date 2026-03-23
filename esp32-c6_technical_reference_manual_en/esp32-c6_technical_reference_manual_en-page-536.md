

```markdown
Register 14.10. TIMG_WDTCONFIGO_REG (0x0048)

Continued from the previous page...

TIMG_WDT_CPU_RESET_LENGTH Configures the CPU reset signal length. Valid only when write protection is disabled.
Measurement unit: mwdt_clk.

|   | Value |
|---|--------|
| 0: | 8      |
| 1: | 16     |
| 2: | 24     |
| 3: | 32     |
| 4: | 40     |
| 5: | 64     |
| 6: | 128    |
| 7: | 256    |

(R/W)

TIMG_WDT_CONF_UPDATE_EN Configures to update the WDT configuration registers.

- O: No effect
- 1: Update (WT)

TIMG_WDT_STG3 Configures the timeout action of stage 3. See details in TIMG_WDT_STGO. Valid only when write protection is disabled. (R/W)

TIMG_WDT_STG2 Configures the timeout action of stage 2. See details in TIMG_WDT_STGO. Valid only when write protection is disabled. (R/W)

TIMG_WDT_STG1 Configures the timeout action of stage 1. See details in TIMG_WDT_STGO. Valid only when write protection is disabled. (R/W)

TIMG_WDT_STGO Configures the timeout action of stage 0. Valid only when write protection is disabled.

- O: No effect
- 1: Interrupt
- 2: Reset CPU
- 3: Reset system

(R/W)

TIMG_WDT_EN Configures whether or not to enable the MWDT. Valid only when write protection is disabled.

- O: Disable
- 1: Enable

(R/W)
```