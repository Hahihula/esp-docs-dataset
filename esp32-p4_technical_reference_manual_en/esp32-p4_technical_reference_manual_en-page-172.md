

```markdown
Chapter 1 High-Performance CPU

GoBack

1.13.6.2 Functional Description

To save power, each CPU core can enter a sleep state by executing the WFI instruction. It can be awakened by three types of events: an interrupt, a halt request, or a signal from its dedicated wake-up input port. A high-level pulse lasting a single clock cycle on this dedicated port is sufficient to wake the corresponding core.

For details on how to configure this port, please refer to Chapter 20 System Registers (SYSREG).

Espressif Systems

Submit Documentation Feedback
```