

```markdown
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| BUS_MONITOR_CORE_O_RCD_PDEBUGSP_REG        | HP CPU SP logging register                                                  | 0x004C    | RO     |
| **CPU status registers**                   |                                                                             |           |        |
| BUS_MONITOR_CORE_O_LASTPC_BEFORE_EXCEPTION_REG | PC of the last command before HP CPU enters exception                      | 0x0070    | RO     |
| BUS_MONITOR_CORE_O_DEBUG_MODE_REG          | HP CPU debug mode status register                                          | 0x0074    | RO     |
| **Clock control register**                 |                                                                             |           |        |
| BUS_MONITOR_CLOCK_GATE_REG                 | Clock control register                                                     | 0x0108    | R/W    |
| **Version control register**               |                                                                             |           |        |
| BUS_MONITOR_DATE_REG                       | Version control register                                                   | 0x03FC    | R/W    |
```