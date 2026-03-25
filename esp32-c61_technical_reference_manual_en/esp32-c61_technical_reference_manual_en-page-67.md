

```markdown
Register 1.60. mexstatus (0x7E1)

EXPT_VLD  This bit is automatically set upon entering a trap handler.
This bit is only writable from debug mode.
(RO)

LOCKUP  This bit is automatically set when double exceptions occur.
Upon lockup, the core will stall and wait for the debugger to resolve the lockup.
This bit is only writable from debug mode.
(RO)

BUS_ERR  This bit is automatically set upon entering a load/store fault trap due to a bus error exception.
Upon entering the trap handler, this bit must be read to find if the load/store fault is due to a bus error.
When mexstatus.NMFT is enabled, this bit gets cleared automatically on executing MRET instruction.
When mexstatus.NMFT is disabled and mexstatus.PBXE, this bit must be cleared manually before resuming execution, else it may re-trigger a pending bus error exception.
(R/W)

PBEXE  Configures whether to enable the pending bus-error exception.
0: Disable
1: Enable
(R/W) When mexstatus.PBXE is enabled and mexstatus.NMFT is disabled, a synchronous exception is generated when mexstatus.BUS_ERR is set.
If mexstatus.NMFT is enabled, mexstatus.PBXE has no effect.
Upon entering a trap the value of mexstatus.PBXE is pushed into mexstatus.PPBEXE and mexstatus.PBXE is set to 0, automatically.
Upon exiting a trap via MRET, the value of mexstatus.PPBEXE is popped back into mexstatus.PBXE.
(R/W)

PPBEXE  Configures whether to enable the previous pending bus-error exception.
0: Disable
1: Enable
Upon entering a trap, the value of mexstatus.PBXE is pushed into mexstatus.PPBEXE.
Upon exiting a trap via MRET, the value of mexstatus.PPBEXE is popped back into mexstatus.PBXE and mexstatus.PPBEXE is set to 1, automatically.
(R/W)

Continued on the next page...
```