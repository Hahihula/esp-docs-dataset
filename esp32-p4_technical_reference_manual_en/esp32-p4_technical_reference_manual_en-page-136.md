

```markdown
| Name          | Description                                                                 | Address   | Access |
|---------------|-----------------------------------------------------------------------------|-----------|--------|
| pmcfg0        | Physical memory protection configuration register                           | 0x3A0     | R/W    |
| pmcfg1        | Physical memory protection configuration register                           | 0x3A1     | R/W    |
| pmcfg2        | Physical memory protection configuration register                           | 0x3A2     | R/W    |
| pmcfg3        | Physical memory protection configuration register                           | 0x3A3     | R/W    |
| pmcfg4        | Physical memory protection configuration register                           | 0x3A4     | R/W    |
| pmcfg5        | Physical memory protection configuration register                           | 0x3A5     | R/W    |
| pmcfg6        | Physical memory protection configuration register                           | 0x3A6     | R/W    |
| pmcfg7        | Physical memory protection configuration register                           | 0x3A7     | R/W    |
| pmpaddrn      | Physical memory protection address register (n: 0-31)                        | 0x3B0+0x1*n | R/W    |

### Register Description

PMP unit implements all pmcfg0-3 and pmpaddr0-15 CSRs as defined in RISC-V Instruction Set Manual, Volume II: Privileged Architecture, Version 1.10.

#### Register 1.108. pmcfg0 (0x3A0)

```markdown
┌──────────────┬────────┬────────┬────────┬────────┬────────┐
│ pmp3cfg      │        │ pmp2cfg│        │ pmp1cfg│        │ pmp0cfg│
├──────────────┼────────┼────────┼────────┼────────┼────────┤
│ 31           │ 24     │ 23     │ 16     │ 15     │ 8      │ 7      │ 0      │
├──────────────┼────────┼────────┼────────┼────────┼────────┼────────┼────────┤
│             │        │        │        │        │        │ Reset   │
└──────────────┴────────┴────────┴────────┴────────┴────────┴────────┘

pmp3cfg Configuration register for PMP entry 3. (R/W)
pmp2cfg Configuration register for PMP entry 2. (R/W)
pmp1cfg Configuration register for PMP entry 1. (R/W)
pmp0cfg Configuration register for PMP entry 0. (R/W)

#### Register 1.109. pmcfg1 (0x3A1)

```markdown
┌──────────────┬────────┬────────┬────────┬────────┬────────┐
│ pmp7cfg      │        │ pmp6cfg│        │ pmp5cfg│        │ pmp4cfg│
├──────────────┼────────┼────────┼────────┼────────┼────────┤
│ 31           │ 24     │ 23     │ 16     │ 15     │ 8      │ 7      │ 0      │
├──────────────┼────────┼────────┼────────┼────────┼────────┼────────┼────────┤
│             │        │        │        │        │        │ Reset   │
└──────────────┴────────┴────────┴────────┴────────┴────────┴────────┘

pmp7cfg Configuration register for PMP entry 7. (R/W)
pmp6cfg Configuration register for PMP entry 6. (R/W)
pmp5cfg Configuration register for PMP entry 5. (R/W)
pmp4cfg Configuration register for PMP entry 4. (R/W)
```