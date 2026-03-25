

```markdown
| Internal Interrupt Source | Trigger Condition                                                                                                                                                                                                                       | Interrupt Signal |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|
|                            |                                                                                                                                                                                                                                           |                  |
| TRACE_MEM_FULL_INTR       | Triggered when the packet size exceeds the capacity of the trace memory, namely when `TRACE_MEM_CURRENT_ADDR_REG` reaches the value of `TRACE_MEM_END_ADDR_REG`. If necessary, this interrupt can be enabled to notify the HP CPU for processing, such as applying for a new memory space again. | TRACE_INTR      |
| TRACE_FIFO_OVERFLOW_INTR  | Triggered when the internal FIFO overflows and one or more packets have been lost.                                                                                                                                                    | TRACE_INTR      |

Note:
For definitions of *interrupt*, *interrupt signal*, *interrupt source*, and their correlations, please refer to Chapter 11 Interrupt Matrix > Section 11.2 Terminology.
```

## 3.8 Programming Procedures

### 3.8.1 Encoder Option Configuration

By default, trace packets are sent to memory with deltas address until the trace FIFO overflows or the trace memory becomes full. There are some optional configuration options that can change the trace behavior.

*   **Full address mode**
    - The encoder uses delta address mode by default. Users can set `TRACE_FULL_ADDRESS` to enable full address mode for debugging.
*   **Restart after packet loss**
    - Once the trace packet is lost due to FIFO overflow, the encoder will automatically stop if `TRACE_RESTART_ENA` is set. When the FIFO is empty, the encoder will restart to report packets.
*   **Stall CPU while FIFO is almost full**
    - If `TRACE_STALL_ENA` is set, when the FIFO is almost full, a stall request will be asserted to the CPU, and the CPU will be stalled until the request is deasserted.
*   **Stop tracing when the CPU is halted**
    If `TRACE_HALT_ENA` is set, when the CPU is halted, the encoder will output a packet to report the address of the last instruction before halting, followed by a support packet to indicate that tracing has stopped. Upon the deassertion of the halted signal, the encoder will start tracing again, commencing with a synchronization packet.
```