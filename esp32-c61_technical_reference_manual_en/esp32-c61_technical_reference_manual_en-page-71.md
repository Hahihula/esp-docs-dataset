

```markdown
Register 1.68. stpc2 (0xBF2)

| 31 | ADDR | VLD |
|----|------|-----|
|    | 0x00000000 | 1   | 0 |
|    |         | Reset |

VLD Configures whether the program-counter address value in this CSR is valid for a recent store bus-error exception.
O: Not valid
1: Valid
(R/W)

ADDR Configures the higher 31 bits of the half-word-aligned program counter corresponding to the same store bus-error exception. (R/W)


Register 1.69. sttval0 (0xBF8)

| 31 | ADDR |
|----|------|
|    | 0x00000000 |
|    | Reset |

ADDR Configures the access address corresponding to the store bus-error exception recorded in stpc0. (R/W)


Register 1.70. sttval1 (0xBF9)

| 31 | ADDR |
|----|------|
|    | 0x00000000 |
|    | Reset |

ADDR Configures the access address corresponding to the store bus-error exception recorded in stpc1. (R/W)


Register 1.71. sttval2 (0xBFA)

| 31 | ADDR |
|----|------|
|    | 0x00000000 |
|    | Reset |

ADDR Configures the access address corresponding to the store bus-error exception recorded in stpc2. (R/W)
```