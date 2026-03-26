

```markdown
Chapter 1 High-Performance CPU

GoBack

1.13.3 RunStall Support

1.13.3.1 Overview

The RunStall signal allows an external agent to stall the processor and shut off much of the clock tree to save operating power. The RunStall input allows external logic to stall the processor’s internal pipeline. Any in-progress instructions in the pipeline will complete after the assertion of the RunStall input line. After the pipeline is stalled, the core outputs a handshake signal “corestalled” to indicate successful stalling of the CPU pipeline.

1.13.3.2 Functional Description

The RunStall input can be used in the following two scenarios:

* As a mechanism to initialize instruction and data RAMs after a reset. If the RunStall input is asserted during reset and remains asserted after the reset is removed, the processor will be in a stalled state. Instruction and data RAMs can be initialized and after these RAMs have been initialized, the RunStall can be released, allowing the processor to start code execution. This mechanism allows the processor’s reset vector to point to an address in local instruction RAM, and the reset code can be written to the instruction RAM by an external agent before the processor starts executing code.

* To freeze the processor’s internal pipeline. Assertion of RunStall reduces the processor’s active power dissipation without using or requiring interrupts and the WAITI option. However, the power savings resulting from use of the RunStall signal will not be as great as for those using WAITI, because the RunStall logic allows some portions of the processor to be active even though the pipeline is stalled.

Figure 1.13-1 shows the timing diagram for RunStall and CoreStalled signals and CPU core state transition.

![Figure 1.13-1. CPU Core State Transition Using RunStall](image)

1.13.3.3 Register Summary

The SoC registers in Section 20.2.1.10 can be used to assert RunStall to HP cores.
```