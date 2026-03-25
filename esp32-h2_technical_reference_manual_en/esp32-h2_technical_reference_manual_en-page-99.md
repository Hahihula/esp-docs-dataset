

```markdown
Chapter 2 RISC-V Trace Encoder (TRACE)

Register 2.4. TRACE_MEM_ADDR_UPDATE_REG (0x000C)

TRACE_MEM_CURRENT_ADDR_UPDATE Configures whether to update the current memory address to the start address of the memory.
O: Not update
1: Update
(WT)

Register 2.5. TRACE_FIFO_STATUS_REG (0x0010)

TRACE_FIFO_EMPTY Represents the FIFO status.
O: Not empty
1: Empty
(RO)

TRACE_WORK_STATUS Represents the encoder status.
O: Not tracing instruction
1: Tracing instructions and reporting packets
(RO)
```