

```markdown
Chapter 3 RISC-V Trace Encoder (TRACE)

GoBack

3.2 Introduction

In complex systems, understanding program execution flow is not straightforward. This may be due to a number of factors, for example, interactions with other cores, peripherals, real-time events, poor implementations, or some combination of all of the above.

It is hard to use a debugger to monitor the program execution flow of a running system in real time, as this is intrusive and might affect the running state. However, it is important to provide the visibility of program execution.

That is where instruction trace comes in, which provides a trace of the program execution. It works by tracking execution from a known start address and sending messages about the address deltas taken by the program. These deltas are typically introduced by jump, call, return, and branch type instructions, although interrupts and exceptions are also types of deltas.

Figure 3.2-1 shows the instruction delta trace flow.

* The HP CPU core provides an instruction trace interface that outputs the instruction information executed by the HP CPU. Such information includes instruction address, instruction type, etc. For more details about ESP32-C5 HP CPU’s instruction trace interface, please refer to Chapter 2 High-Performance CPU.
* The trace encoder collects the relevant instruction trace information from HP CPU’s instruction trace interface, compresses the information into lower bandwidth packets, and then stores the packets in system memory.
* The debugger (debug host) can dump the trace packets from the system memory via JTAG or USB Serial/JTAG, and use a decoder to decompress and reconstruct the program execution flow. The trace decoder, usually software on an external PC, takes in the trace packets and reconstructs the program instruction flow with the program binary that runs on the originating hart. This decoding step can be done offline or in real time while the hart is executing.

Figure 3.2-1 Trace Flow Overview

Espressif Systems
Submit Documentation Feedback
ESP32-C5 TRM (Version 1.0)
```