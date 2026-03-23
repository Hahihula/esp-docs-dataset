

```markdown
# 1.5 Interrupt Controller

## 1.5.1 Features

The interrupt controller allows capturing, masking and dynamic prioritization of interrupt sources routed from peripherals to the RISC-V CPU. It supports:

- Up to 31 asynchronous interrupts with unique IDs (1-31)
- Configurable via read/write to memory mapped registers
- 15 levels of priority, programmable for each interrupt
- Support for both level and edge type interrupt sources
- Programmable global threshold for masking interrupts with lower priority
- Interrupts IDs mapped to trap-vector address offsets

For the complete list of interrupt registers and detailed configuration information, please refer to Chapter 8 *Interrupt Matrix (INTERRUPT)*, section 8.4, register group “CPU Interrupt Registers”.

## 1.5.2 Functional Description

Each interrupt ID has 5 properties associated with it:

1. Enable State (0-1):
    - Determines if an interrupt is enabled to be captured and serviced by the CPU.
    - Programmed by writing the corresponding bit in `INTERRUPT_COREO_CPU_INT_ENABLE_REG`.

2. Type (0-1):
    - Enables latching the state of an interrupt signal on its rising edge.
    - Programmed by writing the corresponding bit in `INTERRUPT_COREO_CPU_INT_TYPE_REG`.
    - An interrupt for which type is kept 0 is referred as a ‘level’ type interrupt.
    - An interrupt for which type is set to 1 is referred as an ‘edge’ type interrupt.

3. Priority (1-15):
    - Determines which interrupt, among multiple pending interrupts, the CPU will service first.
    - Programmed by writing to the `INTERRUPT_COREO_CPU_INT_PRI_n_REG` for a particular interrupt ID *n* in range (1-31).
    - Enabled interrupts with priorities zero or less than the threshold value in `INTERRUPT_COREO_CPU_INT_THRESH_REG` are masked.
    - Priority levels increase from 1 (lowest) to 15 (highest).
    - Interrupts with same priority are statically prioritized by their IDs, lowest ID having highest priority.

4. Pending State (0-1):
    - Reflects the captured state of an enabled and unmasked interrupt signal.
```