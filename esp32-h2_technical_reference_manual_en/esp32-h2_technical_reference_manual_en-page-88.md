

```markdown
- Two synchronization modes:
    - synchronization counter counts by packet
    - synchronization counter counts by cycle
- Trace lost status to indicate packet loss
- Automatic restart after packet loss
- Memory writing in loop or non-loop mode
- Two interrupts:
    - Triggered when the packet size exceeds the configured memory space
    - Triggered when a packet is lost
- FIFO (128 × 8 bits) to buffer packets

Table 2.3-1. Trace Encoder Parameters

| Parameter Name         | Value | Description                                                                 |
|------------------------|-------|-----------------------------------------------------------------------------|
| arch_p                 | 0     | Initial version                                                             |
| bpred_size_p           | 0     | Branch prediction mode is not supported                                    |
| cache_size_p           | 0     | Jump target cache mode is not supported                                    |
| call_counter_size_p    | 0     | Implicit return mode is not supported                                      |
| ctype_width_p          | 0     | Packets contain no context information                                     |
| context_width_p        | 0     | Packets contain no context information                                     |
| ecause_width_p         | 5     | Width of exception cause                                                   |
| ecause_choice_p        | 0     | Multiple choice is not supported                                           |
| fOs_width_p            | 0     | Format O packets are not supported                                         |
| filter_context_p       | 0     |                                                                             |
| filter_excint_p        | 0     | Filter function is not supported                                           |
| filter_privilege_p     | 0     |                                                                             |
| filter_tval_p          | 0     |                                                                             |
| iaddress_lsb_p         | 1     | Compressed instructions are supported                                      |
| iaddress_width_p       | 32    | The instruction bus is 32-bit                                               |
| iretire_width_p        | 1     | Width of the iretire bus                                                    |
| ilastsize_width_p      | 0     | Width of the ilastsize                                                      |
| itype_width_p          | 3     | Width of the itype bus                                                      |
| noncontext_p           | 1     | Exclude context from te_inst packets                                       |
| privilege_width_p      | 1     | Only machine and user mode are supported                                   |
| retires_p              | 1     | Maximum number of instructions that can be retired per block                |
| return_stack_size_p    | 0     | Implicit return mode is not supported                                      |
| sijump_p               | 0     | Sequentially inferable jump mode is not supported                          |
| taken_branches_p       | 1     | Only one instruction retired per cycle                                     |
| impdef_width_p         | 0     | Not implemented                                                             |

For detailed descriptions of the above parameters, please refer to the RISC-V Processor Trace Version 1.0 > Chapter Parameters and Discovery.
```