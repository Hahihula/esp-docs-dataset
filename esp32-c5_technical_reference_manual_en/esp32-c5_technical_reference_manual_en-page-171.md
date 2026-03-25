

```markdown
## 4.4 Debugging

This section describes how to debug and test the LP CPU. Debug support is provided through standard JTAG pins and complies with RISC-V External Debug Support Version 0.13.

For ESP32-C5 system debugging overview, please refer to Chapter 2 High-Performance CPU > Figure 2.10-1.

The user interacts with the Debug Host (e.g., laptop), which is running a debugger (e.g., gdb). The debugger communicates with a Debug Translator (e.g., OpenOCD, which may include a hardware driver) to communicate with Debug Transport Hardware (e.g., ESP-Prog adapter). The Debug Transport Hardware connects the Debug Host to the CPU's Debug Transport Module (DTM) through a standard JTAG interface. The DTM provides access to the debug module (DM) using the Debug Module Interface (DMI).

ESP32-C5 features two DTMs interconnected in a daisy-chain configuration. Specifically, TAP0 connects to the HP CPU, and TAP1 is dedicated to the LP CPU.

The HP DM can debug the HP CPU and the LP DM the LP CPU.

The LP CPU implements four registers for core debugging: `dcsr`, `dpc`, `dscratch0`, and `dscratch1`. All of those registers can only be accessed from debug mode. If software attempts to access them when the LP CPU is not in debug mode, an illegal instruction exception will be triggered.

### 4.4.1 Features

The Low-Power CPU has the following debugging features:

- Provides necessary information about the implementation to the debugger.
- Allows the CPU core to be halted and resumed.
- CPU core registers (including CSRs) can be read/written by the debugger.
- CPU core can be reset through the debugger.
- CPU can be halted on software breakpoint (planted breakpoint instruction).
- Hardware single-stepping.
- Two hardware triggers (which can be used as breakpoints/watchpoints). See Section 4.5 for details.

### 4.4.2 Functional Description

The debugging mechanism adheres to the specification RISC-V External Debug Support Version 0.13. For a detailed description of the debugging features, refer to the specification.

According to the specification, a hart can be in the following states: nonexistent, unavail, running, and halted. By default, the LP CPU is in the unavail state. To connect the LP CPU for debugging, users need to clear the state by configuring the `LPPERI_CPU_REG` register.

### 4.4.3 Register Summary

The following table lists the debug CSRs supported for the LP CPU.

The abbreviations given in Column Access are explained in Section Access Types for Registers.
```