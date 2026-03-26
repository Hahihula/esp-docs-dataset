

```markdown
Register 20.93. LP_SYSTEM_USB_CTRL_REG (0x0100)

LP_SYSTEM_USBOTG2O_IN_SUSPEND Configures whether or not to enable wakeup signals from USB OTG2.O.
- 0: Disable
- 1: Enabled
(R/W)

LP_SYSTEM_USBOTG2O_WAKEUP_CLR Write 1 to clear wakeup signals from USB OTG2.0 to PMU.
(WT)
```

```markdown
Register 20.94. LP_SYSTEM_PAD_COMPO_REG (0x0148)

LP_SYSTEM_DREF_COMPO Configures the internal reference voltage of pad comparator0. (R/W)

LP_SYSTEM_MODE_COMPO Configures the comparison mode for pad comparator0.
- 0: Comparing the main voltage with the external reference voltage
- 1: Comparing the main voltage with the internal reference voltage
(R/W)

LP_SYSTEM_XPD_COMPO Configures whether or not to enable pad comparator0.
- 0: Disable
- 1: Enable
(R/W)
```