

```markdown
Chapter 1 High-Performance CPU

GoBack

1.13.4 Debug Assist Information

The HP CPU core complex provides additional debug information to the Debug Assistant module in ESP32-P4.
For details, please refer to Chapter 21 Debug Assistant.

1.13.5 Core Lock-up

1.13.5.1 Overview

Currently, there is no exception enable register defined in the RISC-V programming model, and when returning from the exception service program to the normal program flow, the exception vector number in the MCAUSE register is not cleared, so software developers cannot easily know whether the CPU is currently processing an exception or running a normal program track by the registers defined in the programming model. To address this concern, a custom LOCKUP field has been implemented. It is readable through the custom CSR.

1.13.5.2 Functional Description

When the CPU responds to an exception, it will determine whether the current program flow is in the exception service program (through EXPT_VLD in MEXSTATUS field). If the CPU is processing an exception and triggers a new exception before returning from the exception service program, the CPU will be locked. When CPU is locked:

- the lock-up signal is set high to inform the SoC that the CPU is in a locked state
- the CPU stops instruction fetch and execution
- the CPU keeps the PC at the instruction PC that triggers the CPU lock
- the LOCKUP field in the MEXSTATUS register is set to 1

In a locked-up state, a debugger can still break in and execute debug commands. It is recommended to reset the core when a lock state is detected.

There are some exceptions to the lock-up rule. Exceptions caused by ECALL or EBREAK, when nested in any exception type, will not trigger CPU lock-up.

1.13.5.3 Register Summary

The `mexstatus.LOCKUP` bit provides lock-up status of individual core.

1.13.5.4 Register Description

Please refer to `mexstatus` CSR.

1.13.6 External Wakeup

1.13.6.1 Overview

Each core features a dedicated input port for wake-up via an external event. This functionality is controlled and configured through registers in the SoC.
```