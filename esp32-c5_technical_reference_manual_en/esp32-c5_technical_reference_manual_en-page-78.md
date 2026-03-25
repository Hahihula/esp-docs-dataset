

```markdown
Register 2.58. stpc2 (0xBF2)

| Bit | Field   | Description                                                                 |
|-----|---------|-----------------------------------------------------------------------------|
| 31  | ADDR    | Configures the higher 31 bits of the half-word-aligned program counter corresponding to the same store bus-error exception. (R/W) |
|     | VLD     | Configures whether the program-counter address value in this CSR is valid for a recent store bus-error exception.<br>0: Not valid<br>1: Valid<br>(R/W) |

Register 2.59. sttval0 (0xBF8)

| Bit | Field   | Description                                                                 |
|-----|---------|-----------------------------------------------------------------------------|
| 31  | ADDR    | Configures the access address corresponding to the store bus-error exception recorded in stpc0. (R/W) |

Register 2.60. sttval1 (0xBF9)

| Bit | Field   | Description                                                                 |
|-----|---------|-----------------------------------------------------------------------------|
| 31  | ADDR    | Configures the access address corresponding to the store bus-error exception recorded in stpc1. (R/W) |

Register 2.61. sttval2 (0xBFA)

| Bit | Field   | Description                                                                 |
|-----|---------|-----------------------------------------------------------------------------|
| 31  | ADDR    | Configures the access address corresponding to the store bus-error exception recorded in stpc2. (R/W) |
```