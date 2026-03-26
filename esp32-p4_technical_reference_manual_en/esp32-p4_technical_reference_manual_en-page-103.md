

```markdown
Register 1.75. stpc2 (0xBF2)
ADDR VLD

| 31 | 0x00000000 | 1 | 0 |
|----|------------|---|---|
|    |            | Reset |

VLD Configures whether the program-counter address value in this CSR is valid for a recent store bus-error exception.
O: Not valid
1: Valid
(R/W)

ADDR Configures the higher 31 bits of the half-word-aligned program counter corresponding to the same store bus-error exception. (R/W)
```

```markdown
Register 1.76. sttval0 (0xBF8)
ADDR

| 31 | 0x00000000 | Reset |

ADDR Configures the access address corresponding to the store bus-error exception recorded in stpc0. (R/W)
```

```markdown
Register 1.77. sttval1 (0xBF9)
ADDR

| 31 | 0x00000000 | Reset |

ADDR Configures the access address corresponding to the store bus-error exception recorded in stpc1. (R/W)
```

```markdown
Register 1.78. sttval2 (0xBFA)
ADDR

| 31 | 0x00000000 | Reset |

ADDR Configures the access address corresponding to the store bus-error exception recorded in stpc2. (R/W)
```

Espressif Systems
Submit Documentation Feedback
ESP32-P4 TRM
PRELIMINARY
```