

```markdown
## 2.8 Programming Procedures

### 2.8.1 Enable Encoder

- Configure the address space for the trace memory via `TRACE_MEM_START_ADDR_REG` and `TRACE_MEM_END_ADDR_REG`
- Update the value of `TRACE_MEM_CURRENT_ADDR_REG` to the value of `TRACE_MEM_START_ADDR_REG` by setting `TRACE_MEM_CURRENT_ADDR_UPDATE`
- (Optional) Configure the memory writing mode via the `TRACE_MEM_LOOP` bit of `TRACE_TRIGGER_REG`
  - 0: Non-loop mode
  - 1: Loop mode (default)
- Configure the synchronization mode via the `TRACE_RESYNC_MODE` bit of `TRACE_RESYNC_PROLONGED_REG`
  - 0: count by cycle (default)
  - 1: count by packet
- (Optional) Configures the threshold for the synchronization counter (default value is 128) via `TRACE_RESYNC_PROLONGED_REG`
- (Optional) Enable Interrupt
  - Set the corresponding bit of `TRACE_INTR_ENA_REG` to enable the corresponding interrupt
  - Set the corresponding bit of `TRACE_INTR_CLR_REG` to clear the corresponding interrupt
  - Read `TRACE_INTR_RAW_REG` to know which interrupt occurs
- (Optional) Enable automatic restart by setting the `TRACE_RESTART_ENA` bit of `TRACE_TRIGGER_REG`. This function is enabled by default
- Enable the trace encoder by setting the `TRACE_TRIGGER_ON` field of `TRACE_TRIGGER_REG`

Once the encoder is enabled, it will keep tracing the HP CPU’s instruction trace interface and writing packets to the trace memory.

### 2.8.2 Disable Encoder

- Disable automatic restart by clearing the `TRACE_RESTART_ENA` bit of `TRACE_TRIGGER_REG`
- Stop the encoder by setting the `TRACE_TRIGGER_OFF` bit of `TRACE_TRIGGER_REG`
- Confirm whether all data in the FIFO have been written into the memory by reading the `TRACE_FIFO_EMPTY` bit

### 2.8.3 Decode Data Packets

- Find the first address to decode
  - Read the `TRACE_MEM_FULL_INTR_RAW` bit of the `TRACE_INTR_RAW_REG` register to know if the trace memory is full
```