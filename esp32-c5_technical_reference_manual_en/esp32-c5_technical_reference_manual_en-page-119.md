

```markdown
Chapter 2 High-Performance CPU

GoBack

## 2.10.3 Trace

### 2.10.3.1 Overview

In order to support non-intrusive software debug, the CPU core provides an instruction trace interface that provides relevant information for offline debug purposes. This interface provides relevant information to the Trace Encoder block, which compresses the information and stores it in memory allocated for it. Software decoders can read this information from trace memory without interrupting the CPU core and re-generate the actual program execution by the CPU core.

### 2.10.3.2 Features

The CPU core supports the instruction trace feature and provides the following information to Trace Encoder as mandated in RISC-V Processor Trace Version 1.0:

* Number of instructions being retired.
* Occurrence of exception and interrupt along with cause and trap values.
* Current privilege level of hart.
* Instruction type of retired instructions for jumps, branches, and return.
* Instruction address for instructions retired before and after program counter changes.
* Trace enabling on trigger hit as per action bit in mcontrol.

### 2.10.3.3 Functional Description

The HP core implements mandatory instruction delta tracing, also known as branch tracing. It works by tracking execution from a known start address by sending information about deltas taken by a program. Deltas are typically introduced by jump, call, return, branch type instructions and also by interrupts and exceptions. All such deltas, along with additional details about cause and actual instructions/addresses, are communicated over high bandwidth instruction trace interface output from the core. Trace Encoder operates on the information on this trace interface and compresses the information for storage in memory for offline debug by a decoder. More information about the encoding is available in Chapter 3 RISC-V Trace Encoder (TRACE).

The core does not have any internal registers to provide control over the instruction trace interface. All register controls are available in 3 RISC-V Trace Encoder (TRACE) block.
```