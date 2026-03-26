

```markdown
Chapter 2 RISC-V Trace Encoder (TRACE)

Register 2.4. TRACE_MEM_ADDR_UPDATE_REG (0x000C)

TRACE_MEM_CURRENT_ADDR_UPDATE Configures whether to update the value of TRACE_MEM_CURRENT_ADDR to TRACE_MEM_START_ADDR.

O: Not update
1: Update
(WT)

Register 2.5. TRACE_FIFO_STATUS_REG (0x0010)

TRACE_FIFO_EMPTY Represents whether the FIFO is empty.
1: Empty
O: Not empty (RO)

TRACE_WORK_STATUS Represents the state of the encoder:
O: Idle state
1: Working state
2: Wait state because the hart is halted or in reset
3: Lost state
(RO)
```