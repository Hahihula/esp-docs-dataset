

```markdown
Chapter 1 High-Performance CPU

This section focuses on HP core debug features. For LP core debug features, please refer to Chapter 3 Low-Power CPU.

The user interacts with the Debug Host (e.g. laptop), which is running a debugger (e.g. GDB). The debugger communicates with a Debug Translator (e.g. OpenOCD, which may include a hardware driver) to communicate with Debug Transport Hardware (e.g. ESP-Prog adapter). The Debug Transport Hardware connects the Debug Host to the HP core's Debug Transport Module (DTM) through standard JTAG interface (bypassing LP core DTM). The DTM provides access to the Debug Module (DM) using the Debug Module Interface (DMI).

The DM allows the debugger to halt selected HP cores. Abstract commands provide access to GPRs (general-purpose registers). The Program Buffer allows the debugger to execute arbitrary code on the core, which allows access to additional CPU core state. Alternatively, additional abstract commands can provide access to additional CPU core state.

Each HP core contains Trigger Module supporting 3 triggers. When trigger conditions are met, respective core will halt spontaneously and inform the debug module that they have halted.

System bus access block allows memory and peripheral register access without affecting either HP core.

1.11.2 Features

The HP CPU supports the following basic debugging features for each HP core:

* Provides necessary information about the implementation to the debugger
* Allows the core to be halted and resumed
* Core registers (including CSRs) can be read/written by debugger
* Core can be debugged from the first instruction executed after reset
* Core can be reset through debugger
* Core can be halted on software breakpoint (planted breakpoint instruction)
* Hardware single-stepping
* Execute arbitrary instructions in the halted core by means of the program buffer. 2-word program buffer is supported
* System bus access is supported through word aligned address access
* Supports three Hardware Triggers (can be used as breakpoints/watchpoints) per HP core as described in Section 1.11.3
* Supports LP core debug through daisy chaining of its JTAG DTM

1.11.3 Functional Description

As mentioned earlier, Debug Scheme conforms to the RISC-V External Debug Support Version 0.13.2 specification. Please refer to it for functional operation details.

1.11.4 JTAG Control

Standard JTAG interface is the only way for DTM to access DM. The hardware provides two JTAG methods: PAD_to_JTAG and USB_to_JTAG.
```