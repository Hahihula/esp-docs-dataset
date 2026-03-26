

```markdown
Chapter 53 Two-Wire Automotive Interface (TWAI)
GoBack

The TWAI controller’s interrupt signal to the interrupt matrix will be asserted whenever one or more interrupt bits are set in the `TWAI_INTERRUPT_REG`, and de-asserted when all bits in `TWAI_INTERRUPT_REG` are cleared. The majority of interrupt bits in `TWAI_INTERRUPT_REG` are automatically cleared when the register is read, except for the Receive Interrupt which can only be cleared when all the messages are released by setting the `TWAI_RELEASE_BUFFER` bit.

Note:
For definitions of interrupt, interrupt signal, interrupt source, and their correlations, please refer to Chapter 12 Interrupt Matrix > Section 12.2 Interrupt Terminology in ESP32-P4.

Each interrupt source can be configured by a common set of registers that are described in Section Interrupt Configuration Registers. The specific registers can be found in Section 53.6 Register Summary.
```