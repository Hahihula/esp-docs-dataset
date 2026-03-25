
```markdown
| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| **Key Registers**                          |                                                                                                  |           |        |
| AES_KEY_0_REG                              | AES key data register 0                                                                          | 0x0000    | R/W    |
| AES_KEY_1_REG                              | AES key data register 1                                                                          | 0x0004    | R/W    |
| AES_KEY_2_REG                              | AES key data register 2                                                                          | 0x0008    | R/W    |
| AES_KEY_3_REG                              | AES key data register 3                                                                          | 0x000C    | R/W    |
| AES_KEY_4_REG                              | AES key data register 4                                                                          | 0x0010    | R/W    |
| AES_KEY_5_REG                              | AES key data register 5                                                                          | 0x0014    | R/W    |
| AES_KEY_6_REG                              | AES key data register 6                                                                          | 0x0018    | R/W    |
| AES_KEY_7_REG                              | AES key data register 7                                                                          | 0x001C    | R/W    |
| **TEXT_IN Registers**                      |                                                                                                  |           |        |
| AES_TEXT_IN_0_REG                          | Source text data register 0                                                                      | 0x0020    | R/W    |
| AES_TEXT_IN_1_REG                          | Source text data register 1                                                                      | 0x0024    | R/W    |
| AES_TEXT_IN_2_REG                          | Source text data register 2                                                                      | 0x0028    | R/W    |
| AES_TEXT_IN_3_REG                          | Source text data register 3                                                                      | 0x002C    | R/W    |
| **TEXT_OUT Registers**                     |                                                                                                  |           |        |
| AES_TEXT_OUT_0_REG                         | Result text data register 0                                                                     | 0x0030    | RO     |
| AES_TEXT_OUT_1_REG                         | Result text data register 1                                                                     | 0x0034    | RO     |
| AES_TEXT_OUT_2_REG                         | Result text data register 2                                                                     | 0x0038    | RO     |
| AES_TEXT_OUT_3_REG                         | Result text data register 3                                                                     | 0x003C    | RO     |
| **Control / Configuration Registers**      |                                                                                                  |           |        |
| AES_MODE_REG                               | Defines key length and encryption / decryption                                                  | 0x0040    | R/W    |
| AES_DMA_ENABLE_REG                         | Selects the working mode of the AES accelerator                                                | 0x0090    | R/W    |
| AES_BLOCK_MODE_REG                         | Defines the block cipher mode                                                                    | 0x0094    | R/W    |
| AES_BLOCK_NUM_REG                          | Block number configuration register                                                            | 0x0098    | R/W    |
| AES_INC_SEL_REG                            | Standard incrementing function register                                                        | 0x009C    | R/W    |
| AES_TRIGGER_REG                            | Operation start controlling register                                                           | 0x0048    | WT     |
| AES_DMA_EXIT_REG                           | Operation exit controlling register                                                            | 0x00B8    | WO     |
| AES_PSEUDO_REG                             | Pseudo-round function configuration register                                                   | 0x00D0    | R/W    |
| **Status Register**                        |                                                                                                  |           |        |
| AES_STATE_REG                              | Operation status register                                                                        | 0x004C    | RO     |
| **Interrupt Registers**                    |                                                                                                  |           |        |
| AES_INT_CLR_REG                            | DMA-AES interrupt clear register                                                                | 0x00AC    | WT     |
| AES_INT_ENA_REG                            | DMA-AES interrupt enable register                                                               | 0x00B0    | R/W    |
```