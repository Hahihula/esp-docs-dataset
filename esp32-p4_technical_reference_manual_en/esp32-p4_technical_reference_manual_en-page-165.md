
```markdown
# 1.13 Custom Features

## 1.13.1 Bus Error Response

### 1.13.1.1 Overview

In the HP core, load/store bus errors are handled as asynchronous exceptions, which means that by the time such an exception is detected, the CPU may have executed some of the instructions after the actual load/store instruction that caused the exception.

Due to the asynchronous nature of these exceptions, handling them requires more context than that available via the standard CSRs mcause, mepc and mtval, which are otherwise sufficient for synchronous exceptions. Therefore, additional CSRs have been provided to allow software to gain all the necessary context required to handle and resume a program that has encountered an asynchronous bus-error exception.

In the following sections, these bus-error-specific CSRs are described and the recommended approach is to gain context about a bus-error exception.

### 1.13.1.2 Functional Description

There are two ways to handle load/store bus errors:

*   Synchronous bus-errors mode:
    When this mode is enabled, (by setting mhint.SBE bit) bus-error exceptions can be handled just like other synchronous exceptions. Therefore, execution traps at the exact PC corresponding to the bus error causing load/store instruction, and mepc holds the same PC.
    The side effect of enabling this mode is that it increases the latency of all load/store instructions.

*   Asynchronous bus-errors mode (default):
    -   For handling bus errors in asynchronous mode, it is recommended (although not necessary) to clear the mexstatus.NMFT bit at startup.
    -   In asynchronous mode, bus errors cause the CPU to enter trap handler with MCAUSE value 5 or 7 (depending upon the type of operation which caused the error), and mepc will hold the PC of the last instruction that was about to be executed when CPU detected the bus error(s) due to (one or more) previously executed load/store instruction(s).
    -   Upon entering the exception handler for cause 5 or 7, the mexstatus.BUS_ERR bit must be checked to confirm if it is due to load/store bus-error. If so, this bit must be cleared to acknowledge.
    -   Next, bits ldpc0.vld, ldpc1.vld, stpc0.vld, stpc1.vld and stpc2.vld must be checked to confirm if they are valid. If so, these must be cleared, and the corresponding address fields (ldpc0.addr, ldpc1.addr, stpc0.addr, stpc1.addr, and stpc2.addr) can be extracted from these CSRs to get the program counters at which these faulting load/store instructions were executed. The CSRs ldtval0, ldtval1, sttval0, sttval1 and sttval2 hold the memory access addresses corresponding to the respective loads/stores. Note that the lower indexed CSRs hold the newest bus errors, while the higher indexed CSRs hold the older bus errors.
    -   Note that, even if the cause is either 5 or 7, both load and store bus error CSRs must be checked as sometimes there are more than one load/store instructions (or misaligned accesses which are split into multiple loads/stores) that have been executed and are in flight. Prior to entering the trap
```