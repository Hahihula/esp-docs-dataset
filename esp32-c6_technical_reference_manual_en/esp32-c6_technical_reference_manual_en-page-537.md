

```markdown
Register 14.11. TIMG_WDTCONFIG1_REG (0x004C)

TIMG_WDT_DIVCNT_RST   Configures whether to reset WDT’s clock divider counter.
    0: No effect
    1: Reset
        (WT)

TIMG_WDT_CLK_PRESCALE   Configures MWDT clock prescaler value. Valid only when write protection is disabled.
MWDT clock period = MWDT’s clock source period * TIMG_WDT_CLK_PRESCALE.
(R/W)
```

```markdown
Register 14.12. TIMG_WDTCONFIG2_REG (0x0050)

TIMG_WDT_STGO_HOLD   Configures the stage 0 timeout value. Valid only when write protection is disabled.
Measurement unit: mwdt_clk.
(R/W)
```