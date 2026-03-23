

```markdown
- Programmed by writing the corresponding bit in `INTPRI_COREO_CPU_INT_TYPE_REG`.
- An interrupt for which type is kept 0 is referred as a 'level' type interrupt.
- An interrupt for which type is set to 1 is referred as an 'edge' type interrupt.
- Local CLINT interrupts are always 'level' type and thus have the corresponding bits reserved in the above register.

4. Priority (0-15):
    - Determines which interrupt, among multiple pending interrupts, the CPU will service first.
    - Programmed by writing to the `INTPRI_COREO_CPU_INT_PRI_n_REG` for an external interrupt with particular interrupt ID `n`.
    - Enabled external interrupts with priorities less than the threshold value in `INTPRI_COREO_CPU_INT_THRESH_REG` are masked.
    - Priority levels increase from 0 (lowest) to 15 (highest).
    - Interrupts with same priority are statically prioritized by their IDs, lowest ID having highest priority.
    - Local CLINT interrupts have static priorities associated with them, and thus have the corresponding priority registers to be reserved.
    - Local CLINT interrupts cannot be masked using the threshold values for either modes.

5. Pending State (0-1):
    - Reflects the captured state of an enabled and unmasked external interrupt signal.
    - For each external interrupt ID the corresponding bit in read-only `INTPRI_COREO_CPU_INT_EIP_STATUS_REG` gives its pending state.
    - For each interrupt ID (local or external), the corresponding bit in the `mip` CSR for M mode interrupts or `uip` CSR for U mode interrupts, also gives its pending state.
        - A pending interrupt will cause CPU to enter trap if no other pending interrupt has higher priority.
        - A pending interrupt is said to be 'claimed' if it preempts the CPU and causes it to jump to the corresponding trap vector address.
        - All pending interrupts which are yet to be serviced are termed as 'unclaimed'.

6. Clear State (0-1):
    - Toggling this will clear the pending state of claimed edge-type interrupts only.
    - Toggled by first setting and then clearing the corresponding bit in `INTPRI_COREO_CPU_INT_CLEAR_REG`.
    - Pending state of a level type interrupt is unaffected by this and must be cleared from source.
    - Pending state of an unclaimed edge type interrupt can be flushed, if required, by first clearing the corresponding bit in `INTPRI_COREO_CPU_INT_ENABLE_REG` and then toggling same bit in `INTPRI_COREO_CPU_INT_CLEAR_REG`.
```
For detailed description of the core local interrupt sources, please refer to Section 1.7.

When CPU services a pending M/U mode interrupt, it:
```