

```markdown
Chapter 1 High-Performance CPU

GoBack

purpose registers). The Program Buffer allows the debugger to execute arbitrary code on the core, which allows access to additional CPU core state. Alternatively, additional abstract commands can provide access to additional CPU core state. ESP-RISC-V core contains Trigger Module supporting 4 triggers. When trigger conditions are met, core will halt spontaneously and inform the debug module that they have halted.

System bus access block allows memory and peripheral register access without using the core.

1.10.2 Features

Basic debug functionality supports below features:

* Provides necessary information about the implementation to the debugger.
* Allows the CPU core to be halted and resumed.
* CPU core registers (including CSRs) can be read/written by debugger.
* CPU can be debugged from the first instruction executed after reset.
* CPU core can be reset through debugger.
* CPU can be halted on software breakpoint (planted breakpoint instruction).
* Hardware single-stepping.
* Execute arbitrary instructions in the halted CPU by means of the program buffer. 16-word program buffer is supported.
* System bus access is supported through word aligned address access.
* Supports four Hardware Triggers (can be used as breakpoints/watchpoints) as described in Section 1.11.
* Supports LP core debug.
* Supports cross-triggering between HP and LP core.

1.10.3 Functional Description

As mentioned earlier, Debug Scheme conforms to RISC-V External Debug Support Specification Version 0.13. Please refer to the specification for functional operation details.

1.10.4 JTAG Control

Standard JTAG interface is the only way for DTM to access DM. The hardware provides two JTAG methods: PAD_to_JTAG and USB_to_JTAG.

* PAD_to_JTAG : means that the JTAG's signal source comes from IO.
* USB_to_JTAG : means that the JTAG's signal source comes from USB Serial/JTAG Controller.

Which JTAG method to use depends on many factors. The following table shows the configuration method.
```