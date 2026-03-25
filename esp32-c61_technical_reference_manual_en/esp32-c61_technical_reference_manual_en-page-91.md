

```markdown
| Name          | Description                                                                 | Address   | Access |
|---------------|-----------------------------------------------------------------------------|-----------|--------|
| pmcfg0        | Physical memory protection configuration register                           | 0x3A0     | R/W    |
| pmcfg1        | Physical memory protection configuration register                           | 0x3A1     | R/W    |
| pmcfg2        | Physical memory protection configuration register                           | 0x3A2     | R/W    |
| pmcfg3        | Physical memory protection configuration register                           | 0x3A3     | R/W    |
| pmpaddrn (n: 0-15) | Physical memory protection address register                               | 0x3B0+0x1*n | R/W    |

#### Register Description

PMP unit implements all pmcfg0-3 and pmpaddr0-15 CSRs as defined in RISC-V Instruction Set Manual, Volume II: Privileged Architecture, Version 1.10.

##### Register 1.86. pmcfg0 (0x3A0)

```markdown
| 31 | 24 | 23 | 16 | 15 | 8 | 7 | 0 |
|----|----|----|----|----|---|---|---|
| 0  |    |    |    |    | 0 |   | Reset |
```

- pmcfg Configuration register for PMP entry 3. (R/W)
- pmcfg Configuration register for PMP entry 2. (R/W)
- pmcfg Configuration register for PMP entry 1. (R/W)
- pmcfg Configuration register for PMP entry 0. (R/W)

##### Register 1.87. pmcfg1 (0x3A1)

```markdown
| 31 | 24 | 23 | 16 | 15 | 8 | 7 | 0 |
|----|----|----|----|----|---|---|---|
| 0  |    |    |    |    | 0 |   | Reset |
```

- pmcfg Configuration register for PMP entry 7. (R/W)
- pmcfg Configuration register for PMP entry 6. (R/W)
- pmcfg Configuration register for PMP entry 5. (R/W)
- pmcfg Configuration register for PMP entry 4. (R/W)
```