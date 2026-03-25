

```markdown
| Field name | Bits | Description |
|------------|------|-------------|
| sign_extend | Variable | The field bits are determined by the branches. The number of bits of sign_extend is as follows: <ul><li>1: 7 bits</li><li>2-3: 5 bits</li><li>4-7: 1 bit</li><li>8-15: 1 bit</li><li>16-32: 31 bits</li></ul> |
```

Format 1- no address, branch_map

The length is 5 bytes.

Table 2.6-8. Packet format 1 without address

```markdown
| Field name | Bits | Description |
|------------|------|-------------|
| format | 2 | 01: includes branch information |
| branches | 5 | Number of valid bits in branch_map. The length of branch_map is 31 bits. Only 0 valid. |
| branch_map | 31 | An array of bits indicating whether branches are taken or not. Bit 0 represents the oldest branch instruction executed. For each bit:<ul><li>0: branch taken</li><li>1: branch not taken</li></ul> |
| sign_extend | 2 | Reserved |
```

## 2.7 Interrupt

*   `TRACE_MEM_FULL_INTR`: Triggered when the packet size exceeds the capacity of the trace memory, namely when `TRACE_MEM_CURRENT_ADDR_REG` reaches the value of `TRACE_MEM_END_ADDR_REG`. If necessary, this interrupt can be enabled to notify the CPU for processing, such as applying for a new memory space again.
*   `TRACE_FIFO_OVERFLOW_INTR`: Triggered when the internal FIFO overflows and one or more packets have been lost.

After enabling the trace encoder interrupts, map them to numbered CPU interrupts through the Interrupt Matrix, so that the CPU can respond to these trace encoder interrupts. For details, please refer to Chapter 9 Interrupt Matrix (INTMTX).

## 2.8 Programming Procedures

### 2.8.1 Enable Encoder

*   Configure the address space for the trace memory via `TRACE_MEM_START_ADDR_REG` and `TRACE_MEM_END_ADDR_REG`
```