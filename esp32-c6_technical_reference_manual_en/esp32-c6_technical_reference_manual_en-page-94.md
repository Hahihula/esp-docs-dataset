

```markdown
## 2.5.3 Memory Writing Mode

When writing the trace memory, the size of the trace packets might exceed the capacity of the memory. In this case, you can choose whether to wrap around the trace memory or not by configuring the memory writing mode:

- Loop mode: When the size of the trace packets exceeds the capacity of the trace memory (namely when `TRACE_MEM_CURRENT_ADDR_REG` reaches the value of `TRACE_MEM_END_ADDR_REG`), the trace memory is wrapped around, so that the encoder loops back to the memory’s starting address `TRACE_MEM_START_ADDR_REG`, and old data in the memory will be overwritten by new data.
- Non-loop mode: When the size of the trace packets exceeds the capacity of the trace memory, the trace memory is not wrapped around. The encoder stops at `TRACE_MEM_END_ADDR_REG`, and old data will be retained.

## 2.5.4 Automatic Restart

When packets are lost due to FIFO overflow, the encoder will stop working and need to be resumed by software. If the `TRACE_RESTART_ENA` bit of `TRACE_TRIGGER_REG` is set, once the FIFO is empty, the encoder can automatically be restarted and does not need to be resumed by software.

If the automatic restart feature is enabled, the encoder will be restarted in any case. Therefore, to disable the encoder, the automatic restart feature must be disabled first by clearing the `TRACE_RESTART_ENA` bit of the `TRACE_TRIGGER_REG` register.

## 2.6 Encoder Output Packets

This section mainly introduces ESP32-C6 trace encoder output packet format. ESP32-C6 only implements mandatory instruction delta tracing. It does not support the following optional features:

- Delta address mode (run-time configurable modes is supported)
- Context information and all context-related fields
- Optional sideband signals
- Trigger outputs from the Debug Module

For details about the above features, please refer RISC-V Processor Trace Version 1.0 (referred to below as the specification).

Figure 2.6-1. Trace packet Format

A packet includes header, index and payload. Header, index and payload are transmitted sequentially in bit stream form, from the fields listed at the top of tables below to the fields listed at the bottom. If a field consists
```