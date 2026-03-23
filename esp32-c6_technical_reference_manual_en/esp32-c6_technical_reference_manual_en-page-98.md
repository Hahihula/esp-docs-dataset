

```markdown
| Field name | Bits | Description |
|:-----------|:------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| address    | 31    | Full instruction address |
| notify     | 1     | ESP32-C6 don't support notification, so this bit is always same with the MSB of address. If the value of this bit is different from notify, it indicates that this packet is reporting the instruction following an uninferable discontinuity and is also the instruction before an exception, privilege change or resync. |
| updiscon   | 1     | The field bits are determined by the branches. The number of bits of sign_extend is as follows: <ul><li>1: 7 bits</li><li>2-3: 5 bits</li><li>4-7: 1 bit</li><li>8-15: 1 bit</li><li>16-32: 31 bits</li></ul> |

Format 1 - no address, branch_map

The length is 5 bytes.

Table 2.6-8. Packet format 1 without address
| Field name | Bits | Description |
|:------------|:------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| format      | 2     | O1: includes branch information |
| branches    | 5     | Number of valid bits in branch_map. The length of branch_map is 31 bits. Only O valid. |
|             | 31    | An array of bits indicating whether branches are taken or not. Bit 0 represents the oldest branch instruction executed. For each bit:<ul><li>O: branch taken</li><li>1: branch not taken</li></ul> |
| branch_map  |       | |
| sign_extend | 2     | Reserved |

## 2.7 Interrupt

*   `TRACE_MEM_FULL_INTR`: Triggered when the packet size exceeds the capacity of the trace memory, namely when `TRACE_MEM_CURRENT_ADDR_REG` reaches the value of `TRACE_MEM_END_ADDR_REG`. If necessary, this interrupt can be enabled to notify the HP CPU for processing, such as applying for a new memory space again.
*   `TRACE_FIFO_OVERFLOW_INTR`: Triggered when the internal FIFO overflows and one or more packets have been lost.

After enabling the trace encoder interrupts, map them to numbered CPU interrupts through the Interrupt Matrix, so that the HP CPU can respond to these trace encoder interrupts. For details, please refer to Chapter 10 Interrupt Matrix (INTMTX).
```