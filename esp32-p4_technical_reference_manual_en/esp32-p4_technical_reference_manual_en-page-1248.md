

```markdown
Chapter 20 System Registers (SYSREG)

LP_SYSTEM_HP_PO_CNNT_RSTN_BYPASS_CTRL: configures whether or not to bypass the following reset sources for the HP CNNT power domain during the Power-On reset.

*   Bit-0: eFuse
*   Bit-1: LP watchdog timer
*   Bit-2: USB (JTAG)
*   Bit-3: USB (UART)
*   Bit-4: Unused
*   Bit-5: Unused
*   Bit-6: HP watchdog timer
*   Bit-7: Software

For details about ESP32-P4's power domains, please refer to Chapter 14 Low-Power Management.

Software System Reset

Configure LP_SYSTEM_SYS_SW_RST to trigger a software system reset.

IOMUX Reset

Configure LP_SYSTEM_IO_MUX_RESET_DISABLE to disable the HP IOMUX reset.

20.2.2.6 Wakeup Control

These registers control the behavior of some PMU wakeup sources.

LP_SYSTEM_USBOTG20_IN_SUSPEND: configures whether or not to enable wakeup signals from USB OTG2.0.

LP_SYSTEM_USBOTG20_WAKEUP_CLR: write 1 to clear wakeup signals from USB OTG2.0 to PMU.

20.2.2.7 LPROM and LP SPM Clock Control

LP_SYSTEM_LP_SPM_ROM_CLK_FORCE_ON: set to force on LP SPM_ROM clock if LP CPU clock is on.

LP_SYSTEM_LP_SPM_RAM_CLK_FORCE_ON: set to force on LP SPM_RAM clock.

20.2.2.8 Analog Voltage Comparator

Analog voltage comparatorx (x = 0, 1) are configured by the following register fields:

*   LP_SYSTEM_XPD_COMPx (x = 0, 1): configures whether or not to enable analog voltage comparatorx.
*   LP_SYSTEM_MODE_COMPx (x = 0, 1): configures the comparison mode:
    *   0: comparing the main voltage with the external reference voltage
    *   1: comparing the main voltage with the internal reference voltage
*   LP_SYSTEM_DREF_COMPx (x = 0, 1): configures the internal reference voltage.
```