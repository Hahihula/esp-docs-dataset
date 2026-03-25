

```markdown
| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| LP_GPIO_FUNC0_OUT_SEL_CFG_REG             | Configuration register for GPIO0 output                                    | 0x02B0  | R/W    |
| LP_GPIO_FUNC1_OUT_SEL_CFG_REG             | Configuration register for GPIO1 output                                    | 0x02B4  | R/W    |
| LP_GPIO_FUNC2_OUT_SEL_CFG_REG             | Configuration register for GPIO2 output                                    | 0x02B8  | R/W    |
| LP_GPIO_FUNC3_OUT_SEL_CFG_REG             | Configuration register for GPIO3 output                                    | 0x02BC  | R/W    |
| LP_GPIO_FUNC4_OUT_SEL_CFG_REG             | Configuration register for GPIO4 output                                    | 0x02C0  | R/W    |
| LP_GPIO_FUNC5_OUT_SEL_CFG_REG             | Configuration register for GPIO5 output                                    | 0x02C4  | R/W    |
| LP_GPIO_FUNC6_OUT_SEL_CFG_REG             | Configuration register for GPIO6 output                                    | 0x02C8  | R/W    |
| LP_GPIO_CLOCK_GATE_REG                    | GPIO clock gate register                                                   | 0x03F8  | R/W    |
| Version Register                          |                                                                             |         |        |
| LP_GPIO_DATE_REG                          | Version control register                                                   | 0x03FC  | R/W    |

### 8.18.5 LP IO MUX Register Summary

The addresses in this section are relative to LP IO MUX base address provided in Table 6.3-2 in Chapter 6 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| **Configure Registers**                    |                                                                             |         |        |
| LP_IO_MUX_GPIO0_REG                        | LP IO MUX configuration register for pin GPIO0                             | 0x0000  | R/W    |
| LP_IO_MUX_GPIO1_REG                        | LP IO MUX configuration register for pin GPIO1                             | 0x0004  | R/W    |
| LP_IO_MUX_GPIO2_REG                        | LP IO MUX configuration register for pin GPIO2                             | 0x0008  | R/W    |
| LP_IO_MUX_GPIO3_REG                        | LP IO MUX configuration register for pin GPIO3                             | 0x000C  | R/W    |
| LP_IO_MUX_GPIO4_REG                        | LP IO MUX configuration register for pin GPIO4                             | 0x0010  | R/W    |
| LP_IO_MUX_GPIO5_REG                        | LP IO MUX configuration register for pin GPIO5                             | 0x0014  | R/W    |
| LP_IO_MUX_GPIO6_REG                        | LP IO MUX configuration register for pin GPIO6                             | 0x0018  | R/W    |
| **Version Register**                       |                                                                             |         |        |
| LP_IO_MUX_DATE_REG                         | Version control register                                                   | 0x01FC  | R/W    |

## 8.19 Registers

### 8.19.1 HP GPIO Matrix Registers

The addresses in this section are relative to HP GPIO matrix base address provided in Table 6.3-2 in Chapter 6 System and Memory.

For how to program reserved fields, please refer to Section VII.
```