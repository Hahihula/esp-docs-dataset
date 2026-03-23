

```markdown
## 1.6 Interrupt Controller

### 1.6.1 Features

The interrupt controller allows capturing, masking and dynamic prioritization of interrupt sources routed from peripherals to the RISC-V CPU. It supports:

- Up to 28 external asynchronous interrupts and 4 core local interrupt sources (CLINT) with unique IDs (0-31)
- Configurable via read/write to memory mapped registers
- Delegable to user mode
- 15 levels of priority, programmable for each interrupt
- Support for both level and edge type interrupt sources
- Programmable global threshold for masking interrupts with lower priority
- Interrupts IDs mapped to trap-vector address offsets

For the complete list of interrupt registers and detailed configuration information, please refer to Chapter 10 *Interrupt Matrix (INTMTX)* > Section 10.4.2.

### 1.6.2 Functional Description

Each interrupt ID has 6 properties associated with it. These properties can be configured for the 28 external interrupts (1-2, 5-6, 8-31), but are static (except mode) for the 4 local CLINT interrupts (0, 3, 4, 7). These properties are as follows:

#### 1. Mode (M/U):

- Determines the mode in which an interrupt is to be serviced.
- Programmed by setting or clearing the corresponding bit in `mideleg` CSR.
    - If the bit is cleared for an interrupt in `mideleg` CSR, then that interrupt will be captured in M mode.
    - If the bit is set for an interrupt in `mideleg` CSR, then it will be delegated to U mode.

#### 2. Enable State (0-1):

- Determines if an interrupt is enabled to be captured and serviced by the CPU.
- Programmed by writing the corresponding bit in `INTPRI_CORE0_CPU_INT_ENABLE_REG`.
- Local CLINT interrupts have the corresponding bits reserved in the memory mapped registers thus they are always enabled at the INTCL level.
- An M mode interrupt (external or local) further needs to be unmasked at core level by setting the corresponding bit in `mie` CSR.
- A U mode interrupt (external or local) further needs to be unmasked at core level by setting the corresponding bits in `uiie` CSR.

#### 3. Type (0-1):

- Enables latching the state of an interrupt signal on its rising edge.
```