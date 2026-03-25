

```markdown
| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| INTMTX_COREO_ECDSA_INTR_MAP_REG           | ECDSA_INTR mapping register                                                 | 0x104   | R/W    |
| INTMTX_COREO_INT_STATUS_O_REG             | Status register for INTMTX sources 0 ~ 31                                   | 0x0108  | RO     |
| INTMTX_COREO_INT_STATUS_1_REG              | Status register for INTMTX sources 32 ~ 63                                  | 0x010C  | RO     |
| INTMTX_COREO_INT_STATUS_1_REG              | Status register for INTMTX sources 64 ~ 65                                  | 0x0110  | RO     |
| INTMTX_COREO_INT_SRC_PASS_IN_SEC_STATUS_O_REG | Delegation Status Register for INTMTX sources 0 ~ 31                       | 0x0114  | RO     |
| INTMTX_COREO_INT_SRC_PASS_IN_SEC_STATUS_1_REG | Delegation Status Register for INTMTX sources 32 ~ 63                      | 0x0118  | RO     |
| INTMTX_COREO_INT_SRC_PASS_IN_SEC_STATUS_2_REG | Delegation Status Register for INTMTX sources 64 ~ 65                      | 0x011C  | RO     |
| INTMTX_COREO_INT_SIG_IDX_ASSERT_IN_SEC_REG | Configuration register for interrupt delegation                            | 0x0120  | R/W    |
| INTMTX_COREO_SECURE_STATUS_REG            | Status register for interrupt delegation                                   | 0x0124  | RO     |
| INTMTX_COREO_CLOCK_GATE_REG               | Clock gating register                                                      | 0x0128  | R/W    |
| Version Register                          |                                                                             |         |        |
| INTMTX_COREO_INTMTX_DATE_REG              | Version control register                                                   | 0x07FC  | R/W    |

## 9.6.2 Software Interrupt Register Summary

The addresses in this section are relative to the software interrupt base address provided in Table 4.3-2 in Chapter 4 System and Memory.

The abbreviations given in column Access are explained in Section Access Types for Registers.
```