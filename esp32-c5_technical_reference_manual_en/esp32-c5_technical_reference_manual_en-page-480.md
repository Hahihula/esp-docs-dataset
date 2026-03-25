

```markdown
| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| INTMTX_COREO_PWM_INTR_MAP_REG             | PWM_INTR mapping register                                                   | 0x104   | R/W    |
| INTMTX_COREO_PCNT_INTR_MAP_REG            | PCNT_INTR mapping register                                                  | 0x108   | R/W    |
| INTMTX_COREO_PARL_IO_TX_INTR_MAP_REG      | PARL_IO_TX_INTR mapping register                                             | 0x10C   | R/W    |
| INTMTX_COREO_PARL_IO_RX_INTR_MAP_REG      | PARL_IO_RX_INTR mapping register                                             | 0x110   | R/W    |
| INTMTX_COREO_SLC0_INTR_MAP_REG            | SLC0_INTR mapping register                                                  | 0x114   | R/W    |
| INTMTX_COREO_SLC1_INTR_MAP_REG            | SLC1_INTR mapping register                                                  | 0x118   | R/W    |
| INTMTX_COREO_DMA_IN_CHO_INTR_MAP_REG      | DMA_IN_CHO_INTR mapping register                                             | 0x11C   | R/W    |
| INTMTX_COREO_DMA_IN_CH1_INTR_MAP_REG      | DMA_IN_CH1_INTR mapping register                                             | 0x120   | R/W    |
| INTMTX_COREO_DMA_IN_CH2_INTR_MAP_REG      | DMA_IN_CH2_INTR mapping register                                             | 0x124   | R/W    |
| INTMTX_COREO_DMA_OUT_CHO_INTR_MAP_REG     | DMA_OUT_CHO_INTR mapping register                                            | 0x128   | R/W    |
| INTMTX_COREO_DMA_OUT_CH1_INTR_MAP_REG     | DMA_OUT_CH1_INTR mapping register                                            | 0x12C   | R/W    |
| INTMTX_COREO_DMA_OUT_CH2_INTR_MAP_REG     | DMA_OUT_CH2_INTR mapping register                                            | 0x130   | R/W    |
| INTMTX_COREO_GPSPI2_INTR_MAP_REG          | GPSPI2_INTR mapping register                                                 | 0x134   | R/W    |
| INTMTX_COREO_AES_INTR_MAP_REG             | AES_INTR mapping register                                                    | 0x138   | R/W    |
| INTMTX_COREO_SHA_INTR_MAP_REG             | SHA_INTR mapping register                                                    | 0x13C   | R/W    |
| INTMTX_COREO_RSA_INTR_MAP_REG             | RSA_INTR mapping register                                                     | 0x140   | R/W    |
| INTMTX_COREO_ECC_INTR_MAP_REG             | ECC_INTR mapping register                                                     | 0x144   | R/W    |
| INTMTX_COREO_ECDSA_INTR_MAP_REG           | ECDSA_INTR mapping register                                                    | 0x148   | R/W    |
| INTMTX_COREO_KM_INTR_MAP_REG              | KM_INTR mapping register                                                      | 0x14C   | R/W    |
| INTMTX_COREO_INT_STATUS_0_REG             | Status register for INTMTX sources 0 ~ 31                                    | 0x0150  | RO     |
| INTMTX_COREO_INT_STATUS_1_REG             | Status register for INTMTX sources 32 ~ 63                                   | 0x0154  | RO     |
| INTMTX_COREO_INT_STATUS_2_REG             | Status register for INTMTX sources 64 ~ 83                                   | 0x0158  | RO     |
| INTMTX_COREO_INT_SRC_PASS_IN_SEC_STATUS_0_REG | Delegation Status Register for INTMTX sources 0 ~ 31                       | 0x015C  | RO     |
| INTMTX_COREO_INT_SRC_PASS_IN_SEC_STATUS_1_REG | Delegation Status Register for INTMTX sources 32 ~ 63                     | 0x0160  | RO     |
| INTMTX_COREO_INT_SRC_PASS_IN_SEC_STATUS_2_REG | Delegation Status Register for INTMTX sources 64 ~ 83                     | 0x0164  | RO     |
| INTMTX_COREO_INT_SIG_IDX_ASSERT_IN_SEC_REG | Configuration register for interrupt delegation                             | 0x0168  | R/W    |
| INTMTX_COREO_SECURE_STATUS_REG            | Status register for interrupt delegation                                     | 0x016C  | RO     |
| INTMTX_COREO_CLOCK_GATE_REG               | INTMTX clock gating configure register                                       | 0x0170  | R/W    |

Version Register
```