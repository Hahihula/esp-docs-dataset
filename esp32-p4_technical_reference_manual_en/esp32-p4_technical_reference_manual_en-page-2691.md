

```markdown
Chapter 53 Two-Wire Automotive Interface (TWAI)
GoBack

Resynchronization

Resynchronization occurs on recessive to dominant edges when the bus is not idle. If the edge has a positive Phase Error (e > 0), PBS1 is lengthened by a certain number of Time Quanta. If the edge has a negative Phase Error (e < 0), PBS2 will be shortened by a certain number of Time Quanta.

The number of Time Quanta to lengthen or shorten depends on the magnitude of the Phase Error, and is also limited by the Synchronization Jump Width (SJW) value which is programmable.

- When the magnitude of the Phase Error (e) is less than or equal to the SJW, PBS1/PBS2 are lengthened/shortened by the e number of Time Quanta. This has the same effect as Hard Synchronization.
- When the magnitude of the Phase Error is greater than the SJW, PBS1/PBS2 are lengthened/shortened by the SJW number of Time Quanta. This means it may take multiple bits of synchronization before the Phase Error is entirely corrected.

53.3 Architectural Overview

The major functional blocks of the TWAI controller are shown in Figure 53.3-1.
```

![Figure 53.3-1. TWAI Overview Diagram](image_path)

```markdown
Configuration | Receive Buffer | Command | Error Management | Interrupt & Status | Transmit Buffer
Host Controller Addr Data Control Registers
Receive FIFO
Acceptance Filter
Bit Stream Processing
Error Management Logic
Bit Timing Logic
CLKOUT RX Standby TX BUS_OFF
TWAI

Figure 53.3-1. TWAI Overview Diagram
```