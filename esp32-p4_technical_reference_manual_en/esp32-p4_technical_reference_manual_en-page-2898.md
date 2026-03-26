

```markdown
| Name                                 | Description                                                                 | Address   | Access |
|--------------------------------------|-----------------------------------------------------------------------------|------------|--------|
| RMT_CHOSTATUS_REG                   | Status register for channel 0                                               | 0x0050     | RO     |
| RMT_CH1STATUS_REG                   | Status register for channel 1                                               | 0x0054     | RO     |
| RMT_CH2STATUS_REG                   | Status register for channel 2                                               | 0x0058     | RO     |
| RMT_CH3STATUS_REG                   | Status register for channel 3                                               | 0x005C     | RO     |
| RMT_CH4STATUS_REG                   | Status register for channel 4                                               | 0x0060     | RO     |
| RMT_CH5STATUS_REG                   | Status register for channel 5                                               | 0x0064     | RO     |
| RMT_CH6STATUS_REG                   | Status register for channel 6                                               | 0x0068     | RO     |
| RMT_CH7STATUS_REG                   | Status register for channel 7                                               | 0x006C     | RO     |

**Interrupt registers**

| Name                                 | Description                                                                 | Address   | Access |
|--------------------------------------|-----------------------------------------------------------------------------|------------|--------|
| RMT_INT_RAW_REG                     | Interrupt raw signal status register                                        | 0x0070     | R/WTC/SS |
| RMT_INT_ST_REG                      | Interrupt signal status register                                             | 0x0074     | RO     |
| RMT_INT_ENA_REG                     | Interrupt enable signal configuration register                               | 0x0078     | R/W    |
| RMT_INT_CLR_REG                     | Interrupt clear signal configuration register                                | 0x007C     | WT     |

**Carrier wave duty cycle registers**

| Name                                 | Description                                                                 | Address   | Access |
|--------------------------------------|-----------------------------------------------------------------------------|------------|--------|
| RMT_CHOCARRIER_DUTY_REG             | Duty cycle configuration register for channel 0                             | 0x0080     | R/W    |
| RMT_CH1CARRIER_DUTY_REG             | Duty cycle configuration register for channel 1                             | 0x0084     | R/W    |
| RMT_CH2CARRIER_DUTY_REG             | Duty cycle configuration register for channel 2                             | 0x0088     | R/W    |
| RMT_CH3CARRIER_DUTY_REG             | Duty cycle configuration register for channel 3                             | 0x008C     | R/W    |

**TX event configuration registers**

| Name                                 | Description                                                                 | Address   | Access |
|--------------------------------------|-----------------------------------------------------------------------------|------------|--------|
| RMT_CHO_TX_LIM_REG                  | Configuration register for channel 0 TX event                               | 0x00A0     | varies |
| RMT_CH1_TX_LIM_REG                  | Configuration register for channel 1 TX event                               | 0x00A4     | varies |
| RMT_CH2_TX_LIM_REG                  | Configuration register for channel 2 TX event                               | 0x00A8     | varies |
| RMT_CH3_TX_LIM_REG                  | Configuration register for channel 3 TX event                               | 0x00AC     | varies |
| RMT_TX_SIM_REG                      | RMT TX synchronous register                                                 | 0x00C4     | R/W    |

**RX event configuration registers**

| Name                                 | Description                                                                 | Address   | Access |
|--------------------------------------|-----------------------------------------------------------------------------|------------|--------|
| RMT_CH4_RX_LIM_REG                  | Configuration register for channel 4 RX event                               | 0x00B0     | R/W    |
| RMT_CH5_RX_LIM_REG                  | Configuration register for channel 5 RX event                               | 0x00B4     | R/W    |
| RMT_CH6_RX_LIM_REG                  | Configuration register for channel 6 RX event                               | 0x00B8     | R/W    |
| RMT_CH7_RX_LIM_REG                  | Configuration register for channel 7 RX event                               | 0x00BC     | R/W    |

**Version register**

| Name                                 | Description                                                                 | Address   | Access |
|--------------------------------------|-----------------------------------------------------------------------------|------------|--------|
| RMT_DATE_REG                        | Version control register                                                    | 0x00CC     | R/W    |
```