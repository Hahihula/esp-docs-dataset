

```markdown
Chapter 2 RISC-V Trace Encoder (TRACE)
GoBack

Chapter 2

RISC-V Trace Encoder (TRACE)

The high-performance CPU (HP CPU) of ESP32-C61 supports the instruction trace interface through the trace encoder. The trace encoder connects to HP CPU’s instruction trace interface, compresses the information into smaller packets, and then stores the packets into internal SRAM.

![Figure 2.0-1. Trace Encoder Overview](image)

Figure 2.0-1. Trace Encoder Overview

2.1 Terminology

To better illustrate the functions of the RISC-V Trace Encoder, the following terms are used in this chapter.

| Term                  | Definition                                                                 |
|-----------------------|-----------------------------------------------------------------------------|
| hart                  | RISC-V hardware thread                                                     |
| branch                | an instruction which conditionally changes the execution flow               |
| uniferable discontinuity (updiscn) | a program counter change that can not be inferred from the program binary alone |
| delta                 | a change in the program counter that is other than the difference between two instructions placed consecutively in memory |
| trap                  | the transfer of control to a trap handler caused by either an exception or an interrupt |
| qualification         | an instruction that meets the filtering criteria passes the qualification, and will be traced |
| te_inst               | the name of the packet type emitted by the encoder                         |
| retire                | the final stage of executing an instruction, when the machine state is updated |
| EPC                   | exception program counter                                                   |

Espressif Systems
124
ESP32-C61 TRM (Pre-release v0.5)
Submit Documentation Feedback PRELIMINARY
```