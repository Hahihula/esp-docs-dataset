

```markdown
Chapter 1 ESP-RISC-V CPU

GoBack

1.12.3 RunStall Support

1.12.3.1 Overview

The RunStall signal allows an external agent to stall the processor and shut off most of the clock tree to save operating power. The RunStall input allows external logic to stall the processor’s internal pipeline. Any in-progress instructions in the pipeline will complete after the assertion of the RunStall input line. After the pipeline is stalled, the core outputs a handshake signal “corestalled” to indicate successful stalling of the CPU pipeline.

1.12.3.2 Functional Description

The RunStall input can be used in the following two scenarios:

- As a mechanism to initialize instruction and data RAMs after a reset. If the RunStall input is asserted during reset and remains asserted after the reset is removed, the processor will be in a stalled state. Instruction and data RAMs can be initialized and after these RAMs have been initialized, the RunStall can be released, allowing the processor to start code execution. This mechanism allows the processor’s reset vector to point to an address in local instruction RAM, and the reset code can be written to the instruction RAM by an external agent before the processor starts executing code.

- To freeze the processor’s internal pipeline. Assertion of RunStall reduces the processor’s active power dissipation without using or requiring interrupts and the WAITI option. However, the power savings resulting from use of the RunStall signal will not be as great as for those using WAITI, because the RunStall logic allows some portions of the processor to be active even though the pipeline is stalled.

Figure 1.12-1 shows the timing diagram for RunStall and CoreStalled signals and CPU core state transition.

cpu_clk | RunStall
--------|--------
CoreStalled | 
CPU STATE | BUSY IDLE BUSY

Figure 1.12-1. CPU Core State Transition Using RunStall

1.12.3.3 Register Summary

The TRACE_STALL_ENA register field in Chapter 2 RISC-V Trace Encoder (TRACE) can be used to assert RunStall to HP core.

1.12.4 Debug Assist Information

The HP CPU core complex provides additional debug information to the Debug Assistant module in ESP32-C61. For details, please refer to Chapter 18 Debug Assistant.

1.12.5 Core Lock-up
```