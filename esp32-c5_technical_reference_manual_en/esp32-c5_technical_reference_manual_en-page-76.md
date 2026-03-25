

```markdown
Register 2.52. ldpc0 (0xBEO)

| 31 | ADDR | VLD |
|----|------|-----|
|    |      | 1   | 0   |
|    |      |     | Reset |

VLD Configures whether the program-counter address value in this CSR is valid for a recent load bus-error exception.
O: Not valid
1: Valid
(R/W)

ADDR Configures the higher 31 bits of the half-word-aligned program counter corresponding to the same load bus-error exception. (R/W)


Register 2.53. ldpc1 (0xBE1)

| 31 | ADDR | VLD |
|----|------|-----|
|    |      | 1   | 0   |
|    |      |     | Reset |

VLD Configures whether the program-counter address value in this CSR is valid for a recent load bus-error exception.
O: Not valid
1: Valid
(R/W)

ADDR Configures the higher 31 bits of the half-word-aligned program counter corresponding to the same load bus-error exception. (R/W)


Register 2.54. Idtval0 (0xBE8)

| 31 | ADDR |
|----|------|
|    |      |
|    | Reset |

ADDR Configures the access address corresponding to the load bus-error exception recorded in ldpc0. (R/W)
```