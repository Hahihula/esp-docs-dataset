

```markdown
Register 1.69. Idpc0 (0xBEO)

ADDR

31 | 1 | 0
---|----|----
0x00000000 | Reset

VLD Configures whether the program-counter address value in this CSR is valid for a recent load bus-error exception.
O: Not valid
1: Valid
(R/W)

ADDR Configures the higher 31 bits of the half-word-aligned program counter corresponding to the same load bus-error exception. (R/W)


Register 1.70. Idpc1 (0xBE1)

ADDR

31 | 1 | 0
---|----|----
0x00000000 | Reset

VLD Configures whether the program-counter address value in this CSR is valid for a recent load bus-error exception.
O: Not valid
1: Valid
(R/W)

ADDR Configures the higher 31 bits of the half-word-aligned program counter corresponding to the same load bus-error exception. (R/W)


Register 1.71. Idtval0 (0xBE8)

ADDR

31 | 0
---|----
0x00000000 | Reset

ADDR Configures the access address corresponding to the load bus-error exception recorded in Idpc0. (R/W)
```