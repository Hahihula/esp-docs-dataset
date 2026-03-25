

```markdown
## 2.2 Introduction

In complex systems, understanding program execution flow is not straightforward. This may be due to a number of factors, such as interactions with other cores, peripherals, real-time events, poor implementations, or some combination of all of the above.

It is hard to use a debugger to monitor the program execution flow of a running system in real-time, as this is intrusive and might affect the running state. But providing visibility of program execution is important.

That is where instruction trace comes in, which provides trace of the program execution.

Figure 2.2-1 shows the schematics of instruction trace:

* The CPU core provides an instruction trace interface that outputs the instruction information executed by the CPU, such as instruction address, instruction type, etc. For more details about ESP32-H2 CPU’s instruction trace interface, please refer to Chapter 1 ESP-RISC-V CPU.
* The trace encoder connects to the CPU’s instruction trace interface and compresses the information into smaller packets, and then stores the packets in system memory.
* The debugger can dump the trace packets from the system memory via JTAG or USB Serial/JTAG, and use a decoder to decompress and reconstruct the program execution flow. The Trace Decoder, usually software on an external PC, takes in the trace packets and reconstructs the program instruction flow with the program binary that runs on the originating hart. This decoding step can be done offline or in real-time while the hart is executing.

This chapter mainly introduces the implementation details of ESP32-H2’s trace encoder.

## 2.3 Features

* Compatible with RISC-V Processor Trace Version 1.0. See Table 2.3-1 for the implemented parameters
* Arbitrary address range of the trace memory size
```