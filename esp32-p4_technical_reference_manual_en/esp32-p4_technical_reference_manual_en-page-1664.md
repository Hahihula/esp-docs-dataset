

```markdown
| Name                                 | Description                                                                 | Address   | Access |
|--------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| ISP_AF_SUM_A_REG                     | AF window A sharpness statistics register                                   | 0x014C    | RO     |
| ISP_AF_SUM_B_REG                     | AF window B sharpness statistics register                                   | 0x0150    | RO     |
| ISP_AF_SUM_C_REG                     | AF window C sharpness statistics register                                   | 0x0154    | RO     |
| ISP_AF_LUM_A_REG                     | AF window A luminance statistics register                                   | 0x0158    | RO     |
| ISP_AF_LUM_B_REG                     | AF window B luminance statistics register                                   | 0x015C    | RO     |
| ISP_AF_LUM_C_REG                     | AF window C luminance statistics register                                   | 0x0160    | RO     |
| ISP_AWBO_WHITE_CNT_REG               | AWB white patch count statistics register                                   | 0x017C    | RO     |
| ISP_AWBO_ACC_R_REG                   | AWB R channel statistics register                                          | 0x0180    | RO     |
| ISP_AWBO_ACC_G_REG                   | AWB G channel statistics register                                          | 0x0184    | RO     |
| ISP_AWBO_ACC_B_REG                   | AWB B channel statistics register                                          | 0x0188    | RO     |
| ISP_HIST_BIN0_REG                    | HIST interval 0 statistics register                                        | 0x01E0    | RO     |
| ISP_HIST_BIN1_REG                    | HIST interval 1 statistics register                                        | 0x01E4    | RO     |
| ISP_HIST_BIN2_REG                    | HIST interval 2 statistics register                                        | 0x01E8    | RO     |
| ISP_HIST_BIN3_REG                    | HIST interval 3 statistics register                                        | 0x01EC    | RO     |
| ISP_HIST_BIN4_REG                    | HIST interval 4 statistics register                                        | 0x01F0    | RO     |
| ISP_HIST_BIN5_REG                    | HIST interval 5 statistics register                                        | 0x01F4    | RO     |
| ISP_HIST_BIN6_REG                    | HIST interval 6 statistics register                                        | 0x01F8    | RO     |
| ISP_HIST_BIN7_REG                    | HIST interval 7 statistics register                                        | 0x01FC    | RO     |
| ISP_HIST_BIN8_REG                    | HIST interval 8 statistics register                                        | 0x0200    | RO     |
| ISP_HIST_BIN9_REG                    | HIST interval 9 statistics register                                        | 0x0204    | RO     |
| ISP_HIST_BIN10_REG                   | HIST interval 10 statistics register                                       | 0x0208    | RO     |
| ISP_HIST_BIN11_REG                   | HIST interval 11 statistics register                                       | 0x020C    | RO     |
| ISP_HIST_BIN12_REG                   | HIST interval 12 statistics register                                       | 0x0210    | RO     |
| ISP_HIST_BIN13_REG                   | HIST interval 13 statistics register                                       | 0x0214    | RO     |
| ISP_HIST_BIN14_REG                   | HIST interval 14 statistics register                                       | 0x0218    | RO     |
| ISP_HIST_BIN15_REG                   | HIST interval 15 statistics register                                       | 0x021C    | RO     |

**Interrupt Registers**

| Name                         | Description                  | Address   | Access |
|------------------------------|------------------------------|-----------|--------|
| ISP_INT_RAW_REG              | Raw interrupt status register | 0x0064    | R/SS/WTC |
|                              |                              |           |        |
| ISP_INT_ST_REG               | Masked interrupt status register | 0x0068    | RO     |
| ISP_INT_ENA_REG              | Interrupt enable register      | 0x006C    | R/W    |
| ISP_INT_CLR_REG              | Interrupt clear register       | 0x0070    | WT     |

**Version Register**

| Name                         | Description                  | Address   | Access |
|------------------------------|------------------------------|-----------|--------|
| ISP_VER_DATE_REG             | Version control register      | 0x0000    | R/W    |

## 36.8.2 MIPI CSI_Bridge Register Summary

The addresses in this section are relative to **MIPI CSI_Bridge** base address provided in Table 7.3-2 in Chapter 7 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                         | Description                  | Address   | Access |
|------------------------------|------------------------------|-----------|--------|
| Clock Gating Control Register |                              |           |        |
```