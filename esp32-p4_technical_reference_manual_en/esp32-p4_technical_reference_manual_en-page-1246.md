

```markdown
Chapter 20 System Registers (SYSREG)

GoBack

20.2.2 LP System Registers

20.2.2.1 LP Timer Stall Control

The LP_SYSTEM_SYSTIMER_STALL_SEL field allows selection of the systimer_stall signal source for the LP timer, choosing between HP CPU0 and HP CPU1:

*   0: from CPU0
*   1: from CPU1

20.2.2.2 Focused Ion Beam (FIB) Control

The LP_SYSTEM_LP_FIB_SEL field allows selection of the control source for the brownout detector and the super watchdog, choosing between the analog system or software register.

*   Bit-1: selects the control source for the brownout detector.
    *   0: controlled by software register
    *   1: controlled by the analog system.
*   Bit-2: selects the control source for the super watchdog.
    *   0: controlled by software register
    *   1: controlled by the analog system.

Configure LP_SYSTEM_DIG_FIB to enable the brownout detector or the super watchdog via software register.

*   Bit-1: write 1 to enable the brownout detector.
*   Bit-2: write 1 to enable the super watchdog.

Read LP_SYSTEM_ANA_FIB to check the FIB state of brownout detector or the super watchdog via analog system (FIB state).

*   Bit-1: brownout detector
*   Bit-2: super watchdog

20.2.2.3 Boot Mode

Configure LP_SYSTEM_FORCE_DOWNLOAD_BOOT to forcibly switch the chip from SPI Boot mode to Joint Download Boot mode.

20.2.2.4 LP CPU Control

Configure the LP CPU via LP_SYSTEM_SYS_CTRL_REG. In particular:

*   LP_SYSTEM_LP_CPU_BOOT_ADDR: configures the boot address of the LP CPU.
*   LP_SYSTEM_LP_CPU_EXC_PC_REG: represents the exception PC address of the LP CPU.
*   LP_SYSTEM_LP_CPU_DBG_PC_REG: represents the current PC address of the LP CPU.
*   LP_SYSTEM_LP_CORE_ERR_RESP_DIS: configures whether or not to disable error response for respective LP CPU buses.

Espressif Systems

1246
Submit Documentation Feedback

ESP32-P4 TRM
PRELIMINARY
```