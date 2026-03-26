

```markdown
# 1.7 Custom Instruction Extensions

## 1.7.1 Hardware Loop

### 1.7.1.1 Overview

HWLP (hardware loop) is the implementation of “For” loop in hardware. A loop is configured with a start and an end address and the number of iterations before its execution. When instruction execution encounters the start address, the loop execution starts. When the end address is executed, it is considered as one loop count and the start address is fetched again. This procedure is repeated until the loop count is equal to the number of iterations configured.

### 1.7.1.2 Features

HWLP has the following features:

- Execution with no extra penalty compared to conditional branch instructions
- Support for two nested HWLPs
- Configurable using a single instruction (lp.setupi) in case of end address within 1 KB from the configuration instruction

### 1.7.1.3 Functional Description

The configuration of HWLP is done either through CSRs or through custom instructions of HWLP, which will be described in detail in subsequent sections. Any HWLP needs to be configured with a start, an end address, and an iteration count.

When a single loop is to be set up, either Loop0 or Loop1 CSRs can be configured. Before setting up a HWLP, configure STATE bits in `mhwloop_state_reg` CSR to any value other than 0 (OFF, default state). Otherwise, accessing HWLP configuration CSRs will cause an illegal instruction exception. To set up and execute HWLP in user mode, URW bit in `mhwloop_state_reg` CSR should be set to 1.

The core supports a maximum of two HWLPs, which can be executed in nested fashion. Each loop is configured separately in this case. Note that, the inner loop has higher priority than the outer loop in case the end instruction of both loops is common. Hardware Loop0 has to be considered as the inner loop and Loop1 as the outer loop while configuring nested loops, as Loop0 has a higher priority than Loop1 in hardware implementation.

The advantage of a HWLP over a conditional branch instruction is that it has zero penalty for its execution. Branch/JUMP instructions use prediction logic for evaluating branch condition and branch/jump address. If a miss-prediction happens, the core pipeline will be flushed and the correct address will be fetched, and thus a few cycles have already been wasted in fetch of the incorrect instructions before flush. As the HWLP does not need prediction of result or target address of conditional branch, it has no penalty, and thus has a higher throughput.

### 1.7.1.4 Instructions/Operations/Modes Supported in HWLP

- Load type instructions
- Store type instructions
```