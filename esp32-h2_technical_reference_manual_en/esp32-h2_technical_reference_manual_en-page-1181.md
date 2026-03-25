
```markdown
| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| FIFO R/W Registers                         |                                                                                                  |           |        |
| RMT_CHODATA_REG                            | The read and write data register for channel 0 by APB FIFO access.                               | 0x0000    | HRO    |
| RMT_CH1DATA_REG                            | The read and write data register for channel 1 by APB FIFO access.                               | 0x0004    | HRO    |
| RMT_CH2DATA_REG                            | The read and write data register for channel 2 by APB FIFO access.                               | 0x0008    | HRO    |
| RMT_CH3DATA_REG                            | The read and write data register for channel 3 by APB FIFO access.                               | 0x000C    | HRO    |
| Configuration Registers                    |                                                                                                  |           |        |
| RMT_CHOCONFO_REG                           | Configuration register 0 for channel 0                                                         | 0x0010    | varies |
| RMT_CH1CONFO_REG                           | Configuration register 0 for channel 1                                                         | 0x0014    | varies |
| RMT_CH2CONFO_REG                           | Configuration register 0 for channel 2                                                         | 0x0018    | R/W    |
| RMT_CH2CONF1_REG                           | Configuration register 1 for channel 2                                                         | 0x001C    | varies |
| RMT_CH3CONFO_REG                           | Configuration register 0 for channel 3                                                         | 0x0020    | R/W    |
| RMT_CH3CONF1_REG                           | Configuration register 1 for channel 3                                                         | 0x0024    | varies |
| RMT_SYS_CONF_REG                           | Configuration register for RMT APB                                                             | 0x0068    | R/W    |
| RMT_REF_CNT_RST_REG                        | Reset register for RMT clock divider                                                           | 0x0070    | WT     |
| Status Registers                            |                                                                                                  |           |        |
| RMT_CHOSTATUS_REG                          | Channel 0 status register                                                                       | 0x0028    | RO     |
| RMT_CH1STATUS_REG                          | Channel 1 status register                                                                       | 0x002C    | RO     |
| RMT_CH2STATUS_REG                          | Channel 2 status register                                                                       | 0x0030    | RO     |
| RMT_CH3STATUS_REG                          | Channel 3 status register                                                                       | 0x0034    | RO     |
| Interrupt Registers                         |                                                                                                  |           |        |
| RMT_INT_RAW_REG                            | Raw interrupt status                                                                             | 0x0038    | R/WTC/SS|
| RMT_INT_ST_REG                              | Masked interrupt status                                                                          | 0x003C    | RO     |
| RMT_INT_ENA_REG                             | Interrupt enable bits                                                                            | 0x0040    | R/W    |
| RMT_INT_CLR_REG                             | Interrupt clear bits                                                                             | 0x0044    | WT     |
| Carrier Wave Duty Cycle Registers           |                                                                                                  |           |        |
| RMT_CHOCARRIER_DUTY_REG                    | Duty cycle configuration register for channel 0                                                | 0x0048    | R/W    |
| RMT_CH1CARRIER_DUTY_REG                    | Duty cycle configuration register for channel 1                                                | 0x004C    | R/W    |
| RMT_CH2_RX_CARRIER_RM_REG                  | Carrier remove register for channel 2                                                           | 0x0050    | R/W    |
| RMT_CH3_RX_CARRIER_RM_REG                  | Carrier remove register for channel 3                                                           | 0x0054    | R/W    |
| TX Event Configuration Registers            |                                                                                                  |           |        |
| RMT_CHO_TX_LIM_REG                          | Configuration register for channel 0 TX event                                                  | 0x0058    | varies |
```