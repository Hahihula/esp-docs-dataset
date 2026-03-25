

```markdown
Register 2.50. mexstatus (0x7E1)

Continued from the previous page...

PMP_ERR  This bit is automatically set upon entering load/store fault trap due to a PMP/PMA exception.
Upon entering the trap handler, this bit must be read to find if the load/store fault is due to PMP/PMA error.
This bit is cleared automatically upon MRET.
(R/W)

FETCH_ERR  This bit is automatically set upon entering the fetch fault trap due to a bus-error exception.
Upon entering the trap handler, this bit must be read to find if the fetch fault is due to bus error.
This bit is cleared automatically upon MRET.
(R/W)

NMFT  Configures whether to disable the memory fence on trap.
1: CPU will enter the trap handler upon exceptions/interrupts without waiting for pending memory load/store operations to finish (Default).
0: CPU will wait for pending memory load/store operations to finish before entering the trap handler.
(R/W)

CLIC_INHV  Configures whether to enable resuming faulting vector table fetch.
0: Disable
1: Enable (default). When it is set, mcause.minhv is used to decide if mepc holds an instruction address or a vector table address.
(R/W)
```

```markdown
Register 2.51. mhint (0x7C5)

SBE  Configures whether to enable the synchronous load/store bus-error exception.
0: Disable
1: Enable
(R/W)
```