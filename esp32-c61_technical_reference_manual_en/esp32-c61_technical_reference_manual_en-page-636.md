

```markdown
Chapter 13 Timer Group (TIMG)

Register 13.10. USB_SERIAL_JTAG_CONFO_REG (0x0018)
```

Continued from the previous page...

```markdown
TIMG_WDT_CONF_UPDATE_EN Configures to update the WDT configuration registers.

O: No effect
1: Update
(WT)

TIMG_WDT_STG3 Configures the timeout action of stage 3. See details in TIMG_WDT_STGO. Valid only when write protection is disabled. (R/W)

TIMG_WDT_STG2 Configures the timeout action of stage 2. See details in TIMG_WDT_STGO. Valid only when write protection is disabled. (R/W)

TIMG_WDT_STG1 Configures the timeout action of stage 1. See details in TIMG_WDT_STGO. Valid only when write protection is disabled. (R/W)

TIMG_WDT_STGO Configures the timeout action of stage 0. Valid only when write protection is disabled.

O: No effect
1: Interrupt
2: Reset CPU
3: Reset system
(R/W)

TIMG_WDT_EN Configures whether or not to enable the MWDT. Valid only when write protection is disabled.

O: Disable
1: Enable
(R/W)
```