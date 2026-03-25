

```markdown
Register 1.90. pmpXcfg

| Bit | Name   | Description                                                                 |
|-----|--------|-----------------------------------------------------------------------------|
| 7   | Reserved | RESERVED                                                                     |
| 5   | XL     | Configures the custom lock bit. Once set, it can only be cleared through a core reset. (R/W) <br> 0: PMP CSR accesses work normally <br> 1: Respective pmpaddr and pmcfg entry is locked and cannot be modified (R/W) |
| 4   | A      | Configures address matching mode. <br> 0: OFF <br> 1: TOR (Top of range) <br> 2: Not Supported <br> 3: NAPOT (Natullary aligned power-of-two region >= 128 Bytes) (R/W) |
| 3   | X      | Configures execute permission. When set, execution from the address range is allowed. (R/W) |
| 2   | W      | Configures write permission. When set, memory writes to the address range are allowed. (R/W) |
| 1   | R      | Configures execute permission. When set, memory reads from the address range are allowed. (R/W) |
| 0   | L      | Configures the lock bit. Once set, it can only be cleared through a core reset. (R/W) |

Register 1.91. pmpaddrn (n: 0-15) (0x3B0+0x1*n)

address Configures the address for pmpaddrn. (R/W)
```