

```markdown
## 3.4 Debugging

This section describes how to debug and test the LP CPU. Debug support is provided through standard JTAG pins and complies with RISC-V External Debug Support Version 0.13.

For ESP32-C6 system debugging overview, please refer to Section 1.10 Debug > Figure 1.10-1.

The user interacts with the Debug Host (e.g. laptop), which is running a debugger (e.g., gdb). The debugger communicates with a Debug Translator (e.g. OpenOCD, which may include a hardware driver) to communicate with Debug Transport Hardware (e.g. ESP-Prog adapter). The Debug Transport Hardware connects the Debug Host to the CPU's Debug Transport Module (DTM) through a standard JTAG interface. The DTM provides access to the debug module (DM) using the Debug Module Interface (DMI).

DM supports multi-core debugging in compliance with the specification RISC-V External Debug Support Version 0.13, and can control the HP CPU and the LP CPU simultaneously. Hart 1 represents the LP CPU. Users can use OpenOCD to select a hart (0: HP CPU, 1: LP CPU) for debugging.

The LP CPU implements four registers for core debugging: `dcsr`, `dpc`, `dscratch0`, and `dscratch1`. All of those registers can only be accessed from debug mode. If software attempts to access them when the LP CPU is not in debug mode, an illegal instruction exception will be triggered.

### 3.4.1 Features

The Low-Power CPU has the following debugging features:

- Provides necessary information about the implementation to the debugger.
- Allows the CPU core to be halted and resumed.
- CPU core registers (including CSRs) can be read/written by the debugger.
- CPU core can be reset through the debugger.
- CPU can be halted on software breakpoint (planted breakpoint instruction).
- Hardware single-stepping.
- Two hardware triggers (which can be used as breakpoints/watchpoints). See Section 3.5 for details.

### 3.4.2 Functional Description

The debugging mechanism adheres to the specification RISC-V External Debug Support Version 0.13. For a detailed description of the debugging features, refer to the specification.

According to the specification, a hart can be in the following states: nonexistent, unavail, running, and halted. By default, the LP CPU is in the unavail state. To connect the LP CPU for debugging, users need to clear the state by configuring the `LPPERI_CPU_REG` register.

### 3.4.3 Register Summary

The following table lists the debug CSRs supported for the LP CPU.
```