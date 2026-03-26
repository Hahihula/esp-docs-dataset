

```markdown
Chapter 1 High-Performance CPU

GoBack

1.11.4 Trace

1.11.4.1 Overview

In order to support non-intrusive software debug, the CPU core provides an instruction trace interface which provides relevant information for offline debug purpose. This interface provides relevant information to Trace Encoder block, which compresses the information and stores in memory allocated for it. Software decoders can read this information from trace memory without interrupting the CPU core and re-generate the actual program execution by the CPU core.

1.11.4.2 Features

The CPU core supports instruction trace feature and provides below information to Trace Encoder as mandated in RISC-V Processor Trace Version 1.0:

* Number of instructions being retired.
* Occurrence of exception and interrupt along with cause and trap values.
* Current privilege level of hart.
* Instruction type of retired instructions for jumps, branches and return.
* Instruction address for instructions retired before and after program counter changes.
* Trace enabling on trigger hit as per action bit in mcontrol.

1.11.4.3 Functional Description

Each HP core implements mandatory instruction delta tracing, also known as branch tracing. It works by tracking execution from a known start address by sending information about deltas taken by a program. Deltas are typically introduced by jump, call, return, branch type instructions and also by interrupts and exceptions. All such deltas along with additional details about cause and actual instructions/addresses are communicated over high bandwidth instruction trace interface output from the core. Trace Encoder operates on the information on this trace interface and compresses the information for storage in memory for offline debug by a decoder. More information about the encoding is available in Chapter 2 RISC-V Trace Encoder (TRACE).

The core does not have any internal registers to provide control over instruction trace interface. All register controls are available in 2 RISC-V Trace Encoder (TRACE) block.
```