

```markdown
| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| **Control and configuration registers**    |                                                                                                  |           |        |
| BITSCRAMBLER_TX_INST_CFG0_REG              | BitScrambler TX core instruction memory address selection register                              | 0x0000    | R/W    |
| BITSCRAMBLER_TX_INST_CFG1_REG              | BitScrambler TX core instruction memory access register                                        | 0x0004    | R/W    |
| BITSCRAMBLER_RX_INST_CFG0_REG              | BitScrambler RX core instruction memory address selection register                              | 0x0008    | R/W    |
| BITSCRAMBLER_RX_INST_CFG1_REG              | BitScrambler RX core instruction memory access register                                        | 0x000C    | R/W    |
| BITSCRAMBLER_TX_LUT_CFG0_REG               | BitScrambler TX core LUT memory address selection register                                      | 0x0010    | R/W    |
| BITSCRAMBLER_TX_LUT_CFG1_REG               | BitScrambler TX core LUT memory access register                                                 | 0x0014    | R/W    |
| BITSCRAMBLER_RX_LUT_CFG0_REG               | BitScrambler RX core LUT memory address selection register                                      | 0x0018    | R/W    |
| BITSCRAMBLER_RX_LUT_CFG1_REG               | BitScrambler RX core LUT memory access register                                                 | 0x001C    | R/W    |
| **Configuration registers**                |                                                                                                  |           |        |
| BITSCRAMBLER_TX_TAILING_BITS_REG          | BitScrambler TX core extra data length register                                                 | 0x0020    | R/W    |
| BITSCRAMBLER_RX_TAILING_BITS_REG          | BitScrambler RX core extra data length register                                                 | 0x0024    | R/W    |
| BITSCRAMBLER_TX_CTRL_REG                   | BitScrambler TX core control register                                                           | 0x0028    | varies |
| BITSCRAMBLER_RX_CTRL_REG                   | BitScrambler RX core control register                                                           | 0x002C    | varies |
| BITSCRAMBLER_SYS_REG                       | Loopback control register                                                                       | 0x00F8    | R/W    |
| **Status registers**                       |                                                                                                  |           |        |
| BITSCRAMBLER_TX_STATE_REG                  | BitScrambler TX core status register                                                            | 0x0030    | varies |
| BITSCRAMBLER_RX_STATE_REG                  | BitScrambler RX core status register                                                            | 0x0034    | varies |
| **Version register**                       |                                                                                                  |           |        |
| BITSCRAMBLER_VERSION_REG                   | Version control register                                                                        | 0x00FC    | R/W    |
```