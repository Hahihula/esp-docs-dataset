

```markdown
## 2.9.1.4 Register Summary

Below is a list of PMP CSRs supported by the CPU. These are only accessible from machine mode.

| Name           | Description                                      | Address   | Access |
|----------------|--------------------------------------------------|-----------|--------|
| `pmpcf g0`     | Physical memory protection configuration register | 0x3A0     | R/W    |
| `pmpcf g1`     | Physical memory protection configuration register | 0x3A1     | R/W    |
| `pmpcf g2`     | Physical memory protection configuration register | 0x3A2     | R/W    |
| `pmpcf g3`     | Physical memory protection configuration register | 0x3A3     | R/W    |
| `pmpaddrn (n: 0-15)` | Physical memory protection address register      | 0x3B0+0x1*n | R/W   |

## 2.9.1.5 Register Description

PMP unit implements all pmpcf g0~3 and pmpaddr0~15 CSRs as defined in RISC-V Instruction Set Manual, Volume II: Privileged Architecture, Version 1.10.

### Register 2.76. `pmcfg0` (0x3A0)

```
pmp3cfg   pmp2cfg   pmp1cfg   pmp0cfg
31        24         16          8           0
+---------+---------+---------+---------+
|    0    |    0    |    0    |    0    |
+---------+---------+---------+---------+
Reset
```

- `pmp3cfg`: Configuration register for PMP entry 3. (R/W)
- `pmp2cfg`: Configuration register for PMP entry 2. (R/W)
- `pmp1cfg`: Configuration register for PMP entry 1. (R/W)
- `pmp0cfg`: Configuration register for PMP entry 0. (R/W)

### Register 2.77. `pmcfg1` (0x3A1)

```
pmp7cfg   pmp6cfg   pmp5cfg   pmp4cfg
31        24         16          8           0
+---------+---------+---------+---------+
|    0    |    0    |    0    |    0    |
+---------+---------+---------+---------+
Reset
```

- `pmp7cfg`: Configuration register for PMP entry 7. (R/W)
- `pmp6cfg`: Configuration register for PMP entry 6. (R/W)
- `pmp5cfg`: Configuration register for PMP entry 5. (R/W)
- `pmp4cfg`: Configuration register for PMP entry 4. (R/W)
```