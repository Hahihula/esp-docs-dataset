

```markdown
Register 16.10. TIMG_WDTCONFIGO_REG (0x0048)

Continued from the previous page...

TIMG_WDT_CPU_RESET_LENGTH Configures the CPU reset signal length. Valid only when write protection is disabled.
Measurement unit: mwdt_clk.

0: 100 ns
1: 200 ns
2: 300 ns
3: 400 ns

4: 500 ns
5: 800 ns
6: 1.6 µs
7: 3.2 µs

(R/W)

TIMG_WDT_CONF_UPDATE_EN Configures to update the WDT configuration registers.
0: No effect
1: Update
(WT)

TIMG_WDT_STG3 Configures the timeout action of stage 3. Valid only when write protection is disabled.
0: No effect
1: Interrupt
2: Reset CPU
3: Reset system
(R/W)

TIMG_WDT_STG2 Configures the timeout action of stage 2. Valid only when write protection is disabled.
0: No effect
1: Interrupt
2: Reset CPU
3: Reset system
(R/W)

TIMG_WDT_STG1 Configures the timeout action of stage 1. Valid only when write protection is disabled.
0: No effect
1: Interrupt
2: Reset CPU
3: Reset system
(R/W)

Continued on the next page...
```