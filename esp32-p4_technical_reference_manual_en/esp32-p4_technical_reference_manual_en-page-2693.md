

```markdown
Chapter 53 Two-Wire Automotive Interface (TWAI)
The configuration registers store various configuration items for the TWAI controller such as bit rates, Operation mode, Acceptance Filter, etc. Configuration registers can only be modified whilst the TWAI controller is in Reset mode (See Section 53.4.1).

Command Registers
The command register is used by the CPU to drive the TWAI controller to initiate certain actions such as transmitting a message or clearing the Receive Buffer. The command register can only be modified when the TWAI controller is in Operation mode (see Section 53.4.1).

Interrupt & Status Registers
The interrupt register indicates what events have occurred in the TWAI controller (each event is represented by a separate bit). The status register indicates the current status of the TWAI controller.

Error Management Registers
The error management registers include error counters and capture registers. The error counter registers represent TEC and REC values. The capture registers will record information about instances where the TWAI controller detects a bus error, or when it loses arbitration.

Transmit Buffer Registers
The transmit buffer is a 13-byte buffer used to store a TWAI message to be transmitted.

Receive Buffer Registers
The Receive Buffer is a 13-byte buffer which stores a single message. The Receive Buffer acts as a window of Receive FIFO, whose first message will be mapped into the Receive Buffer.
Note that the Transmit Buffer registers, Receive Buffer registers, and the Acceptance Filter registers share the same address range (offset 0x0040 to 0x0070). Their access is governed by the following rules:
* When the TWAI controller is in Reset mode, all reads and writes to the address range maps to the Acceptance Filter registers.
* When the TWAI controller is in Operation mode:
    - All reads to the address range maps to the Receive Buffer registers.
    - All writes to the address range maps to the Transmit Buffer registers.

53.4 Functional Description

53.4.1 Modes
The ESP32-P4 TWAI controller has two working modes: Reset mode and Operation mode. Reset mode and Operation mode are entered by setting or clearing the `TWAI_RESET_MODE` bit.

53.4.1.1 Reset Mode
Entering Reset mode is required in order to modify the various configuration registers of the TWAI controller. When entering Reset mode, the TWAI controller is essentially disconnected from the TWAI bus. When in Reset mode, the TWAI controller will not be able to transmit any messages (including error signals). Any transmission in progress is immediately terminated. Likewise, the TWAI controller will not be able to receive any messages either.
```