

```markdown
| Name                                       | Description                          | Address   | Access |
|--------------------------------------------|--------------------------------------|-----------|--------|
| Memory configuration registers             |                                      |           |        |
| TRACE_MEM_START_ADDR_REG                  | Memory start address                 | 0x0000    | R/W    |
| TRACE_MEM_END_ADDR_REG                    | Memory end address                   | 0x0004    | R/W    |
| TRACE_MEM_CURRENT_ADDR_REG                | Memory current address               | 0x0008    | RO     |
| TRACE_MEM_ADDR_UPDATE_REG                 | Memory address update                | 0x000C    | WT     |
| FIFO status register                       |                                      |           |        |
| TRACE_FIFO_STATUS_REG                     | FIFO status register                 | 0x0010    | RO     |
| Interrupt registers                        |                                      |           |        |
| TRACE_INTR_ENA_REG                         | Interrupt enable register            | 0x0014    | R/W    |
| TRACE_INTR_RAW_REG                         | Interrupt raw status register        | 0x0018    | RO     |
| TRACE_INTR_CLR_REG                         | Interrupt clear register              | 0x001C    | WT     |
| Trace configuration registers              |                                      |           |        |
| TRACE_TRIGGER_REG                          | Trace enable register                | 0x0020    | varies |
| TRACE_RESYNC_PROLONGED_REG                 | Resynchronization configuration register | 0x0024   | R/W    |
| Clock gating control and configuration register |                                |           |        |
| TRACE_CLOCK_GATE_REG                       | Clock gating control register        | 0x0028    | R/W    |
| Version register                           |                                      |           |        |
| TRACE_DATE_REG                             | Version control register             | 0x03FC    | R/W    |
```