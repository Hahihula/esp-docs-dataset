

```markdown
Register 52.60. EMACTSTPSTATUS_REG (0x0728)
```

| Bit | Description |
|-----|-------------|
| 31  | (reserved) |
| 3   | TSTRGTERR   |
| 2   | (reserved) |
| 1   | TSTART     |
| 0   | TSSOVF      |

**TSTRGTERR** Represents whether the target time, being programmed in EMACTGTIME2ND_REG and EMACTGTIMENS_REG, is already elapsed.
- 0: Not elapsed
- 1: Elapsed (R/SS/RC)

**TSTART** Represents whether the system time is greater or equal to the value specified in EMACT-GTIME2ND_REG and EMACTGTIMENS_REG.
- 0: Less than the value
- 1: Greater or equal to the value (R/SS/RC)

**TSSOVF** Represents whether the second value of the timestamp has overflowed beyond 0xFFFF_FFFF.
- 0: No overflow
- 1: Overflow (R/SS/RC)
```