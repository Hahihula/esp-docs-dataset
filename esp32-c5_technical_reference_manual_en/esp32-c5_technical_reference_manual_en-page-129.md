

```markdown
## 2.12.4 Debug Assist Information

The HP CPU core complex provides additional debug information to the Debug Assistant module in ESP32-C5. For details, please refer to Chapter 20 Debug Assistant.

## 2.12.5 Core Lock-up

### 2.12.5.1 Overview

Currently, there is no exception enable register defined in the RISC-V programming model, and when returning from the exception service program to the normal program flow, the exception vector number in the MCAUSE register is not cleared, so software developers cannot easily know whether the CPU is currently processing an exception or running a normal program track by the registers defined in the programming model. To address this concern, a custom LOCKUP field has been implemented. It is readable through the custom CSR.

### 2.12.5.2 Functional Description

When the CPU responds to an exception, it will determine whether the current program flow is in the exception service program (through EXPT_VLD in MEXSTATUS field). If the CPU is processing an exception and triggers a new exception before returning from the exception service program, the CPU will be locked. When CPU is locked:

*   the lock-up signal is set high to inform the SoC that the CPU is in a locked state
*   the CPU stops instruction fetch and execution
*   the CPU keeps the PC at the instruction PC that triggers the CPU lock
*   the LOCKUP field in the MEXSTATUS register is set to 1

In a locked-up state, a debugger can still break in and execute debug commands. It is recommended to reset the core when a lock state is detected.

There are some exceptions to the lock-up rule. Exceptions caused by ECALL or EBREAK, when nested in any exception type, will not trigger CPU lock-up.

### 2.12.5.3 Register Summary

The `mexstatus.LOCKUP` bit provides the lock-up status of the individual core.

### 2.12.5.4 Register Description

Please refer to `mexstatus` CSR.
```