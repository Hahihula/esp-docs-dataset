

```markdown
| 31 | UNXTI | 0 |
|-----:|-------:|----:|
|     |       |    |
|| 0x0 || Reset |

UNXTI Represents the next user mode interrupt entry address and configures the interrupt enable status.

This CSR can be used by software to service the next horizontal interrupt for the same privilege mode when it has greater level than the saved interrupt context (held in ucause.UPIL) and greater level than the interrupt threshold of the corresponding privilege mode, without incurring the full cost of an interrupt pipeline flush and context save/restore.

This CSR is designed to be accessed using CSRRSI/CSRRCI instructions, where the value read is a pointer to an entry in the trap handler table and the write back updates the interrupt-enable status. In addition, writes to the unxti have side-effects that update the interrupt context state.

A read of the unxti CSR using CSRR returns either zero, indicating there is no suitable interrupt to service or that the system is not in a CLIC mode, or returns a non-zero address of the entry in the trap handler table for software trap vectoring.

If the CSR instruction that accesses unxti includes a write, the ustatus CSR is the one used for the read-modify-write portion of the operation, while the ucause register's exccode field and the uintstatus.UIIL field can also be updated with the new interrupt id and level. If the interrupt is edge-triggered, then the pending bit is also zeroed.

The unxti CSR is intended to be used inside an interrupt handler after an initial interrupt has been taken and ucause and uepc registers updated with the interrupted context and the ID of the interrupt.

If the pending interrupt is edge-triggered, hardware will automatically clear the corresponding pending bit when the CSR instruction that accesses unxti includes a write. However, if the CSR instruction does not include write side effects, then no state update on any CSR occurs and thus the interrupt pending bit is not zeroed. This behavior allows software to optimize the selection and execution of interrupts using unxti.
(R/W)

Register 1.29. uintthresh (0x047)

| 31 | 24 | 23 | (reserved) | 0 |
|-----:|----:|----:|------------:|----:|
|     |    |    |            || Reset |

|| 0x0 | 0x000000 ||
```
```markdown
TH Configures the 8-bit level threshold of user mode interrupts.

Note that the effective threshold level for user mode interrupts is the maximum of uintthresh.TH and uintstatus.UIIL. All user mode pending interrupts with levels less than or equal to the effective threshold level are not allowed to preempt the execution.
(R/W)
```