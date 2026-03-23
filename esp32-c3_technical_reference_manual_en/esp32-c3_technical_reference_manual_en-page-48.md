

```markdown
## 1.6.2 Features

Basic debug functionality supports below features.

* Provides necessary information about the implementation to the debugger.
* Allows the CPU core to be halted and resumed.
* CPU core registers (including CSR’s) can be read/written by debugger.
* CPU can be debugged from the first instruction executed after reset.
* CPU core can be reset through debugger.
* CPU can be halted on software breakpoint (planted breakpoint instruction).
* Hardware single-stepping.
* Execute arbitrary instructions in the halted CPU by means of the program buffer. 16-word program buffer is supported.
* System bus access is supported through word aligned address access.
* Supports eight Hardware Triggers (can be used as breakpoints/watchpoints) as described in Section 1.7.

## 1.6.3 Functional Description

As mentioned earlier, Debug Scheme conforms to RISC-V External Debug Support Specification version 0.13. Please refer the specs for functional operation details.

## 1.6.4 Register Summary

Below is the list of Debug CSR’s supported by ESP-RV core.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name       | Description                          | Address | Access |
|------------|--------------------------------------|---------|--------|
| dcsr       | Debug Control and Status             | 0x7B0   | R/W    |
| dpc        | Debug PC                             | 0x7B1   | R/W    |
| dscratch0  | Debug Scratch Register 0             | 0x7B2   | R/W    |
| dscratch1  | Debug Scratch Register 1             | 0x7B3   | R/W    |

All the debug module registers are implemented in conformance to RISC-V External Debug Support Specification version 0.13. Please refer it for more details.

## 1.6.5 Register Description

Below are the details of Debug CSR’s supported by ESP-RV core
```