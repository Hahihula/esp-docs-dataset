

```markdown
Register 1.67. mexstatus (0x7E1)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | CLIC_INHv                                                                   |
| 29  | (reserved)                                                                  |
| 28  | NMFT                                                                        |
| 27  | FETCH_ERR                                                                   |
| 26  | PPBEXE                                                                      |
| 25  | PBESE                                                                       |
| 24  | ERR                                                                         |
| 23  | BUS_ERR                                                                     |
| 22  | (reserved)                                                                  |
| 21  | LOCKUP                                                                      |
| 20  | EXPT_VLD                                                                    |
| 19  | (reserved)                                                                  |
| 18  | Reset                                                                       |

EXPT_VLD This bit is automatically set upon entering a trap handler.
This bit is only writable from debug mode.
(RO)

LOCKUP This bit is automatically set when double exceptions occur.
Upon lockup, the core will stall and wait for the debugger to resolve the lockup.
This bit is only writable from debug mode.
(RO)

BUS_ERR This bit is automatically set upon entering a load/store fault trap due to a bus error exception.
Upon entering the trap handler, this bit must be read to find if the load/store fault is due to a bus error.
When mexstatus.NMFT is enabled, this bit gets cleared automatically on executing MRET instruction.
When mexstatus.NMFT is disabled and mexstatus.PBEXE, this bit must be cleared manually before resuming execution, else it may re-trigger a pending bus error exception.
(R/W)

PBEXE Configures whether to enable the pending bus-error exception.
0: Disable
1: Enable
When mexstatus.PBEXE is enabled and mexstatus.NMFT is disabled, a synchronous exception is generated when mexstatus.BUS_ERR is set.
If mexstatus.NMFT is enabled, mexstatus.PBEXE has no effect.
Upon entering a trap the value of mexstatus.PBEXE is pushed into mexstatus.PPBEXE and mexstatus.PBEXE is set to 0, automatically.
Upon exiting a trap via MRET, the value of mexstatus.PPBEXE is popped back into mexstatus.PBEXE.
(R/W)

PPBEXE Configures whether to enable the previous pending bus-error exception.
0: Disable
1: Enable
Upon entering a trap, the value of mexstatus.PBEXE is pushed into mexstatus.PPBEXE.
Upon exiting a trap via MRET, the value of mexstatus.PPBEXE is popped back into mexstatus.PBEXE and mexstatus.PPBEXE is set to 1, automatically.
(R/W)

Continued on the next page...
```