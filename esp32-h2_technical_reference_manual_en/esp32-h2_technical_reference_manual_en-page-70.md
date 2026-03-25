

```markdown
## 1.10.2 Features

Basic debug functionality supports below features:

* Provides necessary information about the implementation to the debugger.
* Allows the CPU core to be halted and resumed.
* CPU core registers (including CSRs) can be read/written by debugger.
* CPU can be debugged from the first instruction executed after reset.
* CPU core can be reset through debugger.
* CPU can be halted on software breakpoint instructions.
* Hardware single-stepping.
* Execute arbitrary instructions in the halted CPU by means of the program buffer. 16-word program buffer is supported.
* System bus access is supported through word aligned address access.
* Supports four Hardware Triggers (can be used as breakpoints/watchpoints) as described in Section 1.11.

## 1.10.3 Functional Description

As mentioned earlier, Debug Scheme conforms to RISC-V External Debug Support Specification version 0.13. Please refer to the specification for functional operation details.

## 1.10.4 JTAG Control

Standard JTAG interface is the only way for DTM to access DM. The hardware provides two JTAG methods: PAD_to_JTAG and USB_to_JTAG.

* PAD_to_JTAG : means that the JTAG's signal source comes from IO.
* USB_to_JTAG : means that the JTAG's signal source comes from USB_Serial_JTAG controller.

Which JTAG method to use depends on many factors. The following table shows the configuration method.
```