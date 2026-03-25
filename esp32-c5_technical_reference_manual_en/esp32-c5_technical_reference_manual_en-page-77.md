

```markdown
Register 2.55. Idtval1 (0xBE9)

ADDR Configures the access address corresponding to the load bus-error exception recorded in ldpc1. (R/W)


Register 2.56. stpc0 (0xBF0)

VLD Configures whether the program-counter address value in this CSR is valid for a recent store bus-error exception.
O: Not valid
1: Valid
(R/W)

ADDR Configures the higher 31 bits of the half-word-aligned program counter corresponding to the same store bus-error exception. (R/W)


Register 2.57. stpc1 (0xBF1)

VLD Configures whether the program-counter address value in this CSR is valid for a recent store bus-error exception.
O: Not valid
1: Valid
(R/W)

ADDR Configures the higher 31 bits of the half-word-aligned program counter corresponding to the same store bus-error exception. (R/W)
```