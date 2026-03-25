

```markdown
| mlnlbits[3:0] | clicintctl[i][7:0] | Interrupt Levels | Interrupt Priorities |
|---------------|--------------------|------------------|----------------------|
| 0             | ppp........        | 255              | 31, 63, 95, 127, 159, 191, 223, 255 |
| 1             | lpp........        | 127, 255         | 31, 63, 95, 127       |
| 2             | llp........        | 63, 127, 191, 255| 31, 63                 |
| 3-8           | 111........        | 31, 63, 95, 127, 159, 191, 223, 255 | 31                  |

## Machine Mode CLIC Registers

| Name             | Description                                                                 | MCLICBASE Offset | Absolute Address | Access |
|------------------|-----------------------------------------------------------------------------|------------------|------------------|--------|
| mcllicfg         | CLIC machine mode global configuration register                              | 0x0000           | 0x20800000       | R/W    |
| clicinfo         | CLIC information register                                                   | 0x0004           | 0x20800004       | RO     |
| clicintip[3]     | Pending register for CLINT software interrupts                               | 0x100C           | 0x2080100C       | R/W    |
| clicintie[3]     | Enable register for CLINT software interrupts                                | 0x100D           | 0x2080100D       | R/W    |
| clicintattr[3]   | Attribute register for CLINT software interrupts                             | 0x100E           | 0x2080100E       | R/W    |
| clicinctl[3]     | Level control register for CLINT software inter-rupts                       | 0x100F           | 0x2080100F       | R/W    |
| clicintip[7]     | Pending register for CLINT timer interrupts                                  | 0x101C           | 0x2080101C       | R/W    |
| clicintie[7]     | Enable register for CLINT timer interrupts                                   | 0x101D           | 0x2080101D       | R/W    |
| clicintattr[7]   | Attribute register for CLINT timer interrupts                                | 0x101E           | 0x2080101E       | R/W    |
```