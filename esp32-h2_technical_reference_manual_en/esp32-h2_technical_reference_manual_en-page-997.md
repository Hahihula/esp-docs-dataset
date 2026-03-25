

```markdown
Chapter 34 Two-wire Automotive Interface (TWAI) GoBack

Clock Generator
   twai_func_clk_sel
CLK_XTAL → CLK_TWAI
CLK_RC_FAST →

Figure 34.3-2. TWAI Clock Generation

34.3.1 Registers Block

The ESP32-H2 CPU accesses peripherals using 32-bit aligned words. However, the majority of registers in the TWAI controller only contain useful data at the least significant byte (bits [7:0]). Therefore, in these registers, bits [31:8] are ignored on writes, and return 0 on reads.

Configuration Registers

The configuration register stores various configuration items for the TWAI controller such as bit rates, Operation mode, Acceptance Filter, etc. Configuration registers can only be modified whilst the TWAI controller is in Reset mode (See Section 34.4.1).

Command Registers

The command register is used by the CPU to drive the TWAI controller to initiate certain actions such as transmitting a message or clearing the Receive Buffer. The command register can only be modified when the TWAI controller is in Operation mode (see Section 34.4.1).

Interrupt & Status Registers

The interrupt register indicates what events have occurred in the TWAI controller (each event is represented by a separate bit). The status register indicates the current status of the TWAI controller.

Error Management Registers

The error management register includes error counters and capture registers. Error counter registers represent TEC and REC values. Capture registers will record information about instances where the TWAI controller detects a bus error, or when it loses arbitration.

Transmit Buffer Registers

The transmit buffer is a 13-byte buffer used to store a TWAI message to be transmitted.

Receive Buffer Registers

The Receive Buffer is a 13-byte buffer which stores a single message. The Receive Buffer acts as a window of Receive FIFO, whose first message will be mapped into the Receive Buffer.

Note that the Transmit Buffer registers, Receive Buffer registers, and the Acceptance Filter registers share the same address range (offset 0x0040 to 0x0070). Their access is governed by the following rules:

* When the TWAI controller is in Reset mode, all reads and writes to the address range maps to the Acceptance Filter registers.
* When the TWAI controller is in Operation mode:
```