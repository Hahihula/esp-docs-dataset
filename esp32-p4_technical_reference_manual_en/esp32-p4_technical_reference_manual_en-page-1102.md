

```markdown
Register 16.10. TIMG_WDTCONFIGO_REG (0x0048)
```

Continued from the previous page...

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