

```markdown
| Parameter Name              | Value | Description                                                                 |
|-----------------------------|-------|-----------------------------------------------------------------------------|
| filter_excint_p             | 1     | Filtering on exception cause or interrupt is supported                      |
| filter_privilege_p          | 1     | Filtering on privilege is supported                                        |
| filter_tval_p               | 1     | Filtering on trap value is supported                                       |
| iaddress_lsb_p              | 1     | Compressed instructions are supported                                      |
| iaddress_width_p            | 32    | The instruction bus is 32-bit                                               |
| iretire_width_p             | 1     | Width of the iretire bus                                                    |
| ilastsize_width_p           | 0     | Width of the ilastsize                                                      |
| itype_width_p               | 3     | Width of the itype bus                                                      |
| nocontext_p                 | 1     | Exclude context from te_inst packets                                       |
| notime_p                    | 1     | Exclude time from te_inst packets                                          |
| privilege_width_p           | 1     | Only machine and user mode are supported                                   |
| retires_p                   | 1     | Maximum number of instructions that can be retired per block               |
| return_stack_size_p         | 0     | Implicit return mode is not supported                                      |
| sijump_p                    | 0     | Sequentially inferable jump mode is not supported                          |
| taken_branches_p            | 1     | Only one instruction retired per cycle                                     |
| impdef_width_p              | 0     | Not implemented                                                             |

For detailed descriptions of the above parameters, please refer to the [Efficient Trace for RISC-V Version 2.0 > Chapter Parameters and Discovery](#).
```

## 2.4 Architectural Overview

This chapter mainly introduces the implementation details of ESP32-C61's trace encoder.

As shown in Figure 2.0-1, the trace encoder contains an encoder, a FIFO, a register configuration module, and a transmission control module.

The encoder receives the HP CPU's instruction information via the instruction trace interface, compresses it into different packets, and writes it to the internal FIFO.

The transmission control module writes the data in the FIFO to the internal SRAM through the AHB bus.

The FIFO is 128 deep and 8-bit wide. When the memory bandwidth is insufficient, the FIFO may overflow, resulting in packet loss. When a packet is lost, the encoder will send a packet to indicate this event. Thereafter, the encoder will stop working till FIFO gets empty. An interrupt will also be generated to indicate this event if it has been enabled.

## 2.5 Functional Description

### 2.5.1 Synchronization

In order to make the trace robust there must be regular synchronization points within the trace. Synchronization is accomplished by sending a full valued instruction address. When the synchronization counter value reaches the value of the `TRACE_RESYNC_PROLONGED` field of the `TRACE_RESYNC_PROLONGED_REG` register, the encoder will send a synchronization packet (format 3 subformat 0, see Section 2.6.3.1).
```