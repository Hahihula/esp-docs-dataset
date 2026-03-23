

```markdown
- For each interrupt ID, the corresponding bit in read-only `INTERRUPT_COREO_CPU_INT_EIP_STATUS_REG` gives its pending state.
- A pending interrupt will cause CPU to enter trap if no other pending interrupt has higher priority.
- A pending interrupt is said to be 'claimed' if it preempts the CPU and causes it to jump to the corresponding trap vector address.
- All pending interrupts which are yet to be serviced are termed as 'unclaimed'.

5. Clear State (0-1):
  - Toggling this will clear the pending state of claimed edge-type interrupts only.
  - Toggled by first setting and then clearing the corresponding bit in `INTERRUPT_COREO_CPU_INT_CLEAR_REG`.
  - Pending state of a level type interrupt is unaffected by this and must be cleared from source.
  - Pending state of an unclaimed edge type interrupt can be flushed, if required, by first clearing the corresponding bit in `INTERRUPT_COREO_CPU_INT_ENABLE_REG` and then toggling same bit in `INTERRUPT_COREO_CPU_INT_CLEAR_REG`.

When CPU services a pending interrupt, it:
- saves the address of the current un-executed instruction in `mepc` for resuming execution later.
- updates the value of `mcause` with the ID of the interrupt being serviced.
- copies the state of `MIE` into `MPIE`, and subsequently clears `MIE`, thereby disabling interrupts globally.
- enters trap by jumping to a word-aligned offset of the address stored in `mtvec`.

Table 1.5-1 shows the mapping of each interrupt ID with the corresponding trap-vector address. In short, the word aligned trap address for an interrupt with a certain $ID = i$ can be calculated as $(mtvec + 4i)$.

Note: $ID = 0$ is unavailable and therefore cannot be used for capturing interrupts. This is because the corresponding trap vector address $(mtvec + 0x00)$ is reserved for exceptions.

Table 1.5-1. ID wise map of Interrupt Trap-Vector Addresses

| ID | Address     | ID | Address     | ID | Address     | ID | Address     |
|----|-------------|----|-------------|----|-------------|----|-------------|
| 0  | NA          | 8  | mtvec + 0x20| 16 | mtvec + 0x40| 24 | mtvec + 0x60|
| 1  | mtvec + 0x04| 9  | mtvec + 0x24| 17 | mtvec + 0x44| 25 | mtvec + 0x64|
| 2  | mtvec + 0x08| 10 | mtvec + 0x28| 18 | mtvec + 0x48| 26 | mtvec + 0x68|
| 3  | mtvec + 0x0c| 11 | mtvec + 0x2c| 19 | mtvec + 0x4c| 27 | mtvec + 0x6c|
| 4  | mtvec + 0x10| 12 | mtvec + 0x30| 20 | mtvec + 0x50| 28 | mtvec + 0x70|
| 5  | mtvec + 0x14| 13 | mtvec + 0x34| 21 | mtvec + 0x54| 29 | mtvec + 0x74|
| 6  | mtvec + 0x18| 14 | mtvec + 0x38| 22 | mtvec + 0x58| 30 | mtvec + 0x78|
| 7  | mtvec + 0x1c| 15 | mtvec + 0x3c| 23 | mtvec + 0x5c| 31 | mtvec + 0x7c|

After jumping to the trap-vector, the execution flow is dependent on software implementation, although it can be presumed that the interrupt will get handled (and cleared) in some interrupt service routine (ISR) and later the normal execution will resume once the CPU encounters MRET instruction.

Upon execution of MRET instruction, the CPU:
```