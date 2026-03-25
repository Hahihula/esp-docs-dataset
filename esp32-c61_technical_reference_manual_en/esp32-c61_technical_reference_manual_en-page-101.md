

```markdown
Chapter 1 ESP-RISC-V CPU

The DM allows the debugger to halt the HP core. Abstract commands provide access to GPRs (general-purpose registers). The Program Buffer allows the debugger to execute arbitrary code on the core, which allows access to additional CPU core state. Alternatively, additional abstract commands can provide access to additional CPU core state.

HP core contains Trigger Module supporting 3 triggers. When trigger conditions are met, respective core will halt spontaneously and inform the debug module that they have halted.

System bus access block allows memory and peripheral register access without affecting either HP core.

1.10.1.2 Features

HP CPU supports the following basic debugging features:

* Provides necessary information about the implementation to the debugger
* Allows the core to be halted and resumed
* Core registers (including CSRs) can be read/written by debugger
* Core can be debugged from the first instruction executed after reset
* Core can be reset through debugger
* Core can be halted on software breakpoint (planted breakpoint instruction)
* Hardware single-stepping
* Execute arbitrary instructions in the halted core by means of the program buffer. 2-word program buffer is supported
* System bus access is supported through word aligned address access
* Supports three Hardware Triggers (can be used as breakpoints/watchpoints) as described in Section 1.10.2

1.10.1.3 Functional Description

As mentioned earlier, Debug Scheme conforms to the RISC-V External Debug Support Version 0.13.2 specification. Please refer to it for functional operation details.

1.10.1.4 JTAG Control

Standard JTAG interface is the only way for DTM to access DM. The hardware provides two JTAG methods: PAD_to_JTAG and USB_to_JTAG.

* PAD_to_JTAG: The JTAG's signal source comes from IO.
* USB_to_JTAG: The JTAG's signal source comes from USB Serial/JTAG Controller.

Which JTAG method to use depends on many factors. The following table shows the configuration method.
```