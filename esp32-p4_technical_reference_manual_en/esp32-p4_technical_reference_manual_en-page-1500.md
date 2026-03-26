

```markdown
| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| **Control/Configuration Registers**        |                                                                                                  |           |        |
| SHA_MODE_REG                              | Configures SHA algorithm                                                                         | 0x0000    | R/W    |
| SHA_T_STRING_REG                          | Initial Hash Value calculation factor t_string (for SHA-512/t)                                    | 0x0004    | R/W    |
| SHA_T_LENGTH_REG                          | Initial Hash Value calculation factor t_length (for SHA-512/t)                                   | 0x0008    | R/W    |
| SHA_CONTINUE_REG                          | Continues SHA operation (only effective in Typical SHA mode)                                     | 0x0014    | WO     |
| SHA_DMA_START_REG                         | Starts the SHA accelerator for DMA-SHA operation                                                 | 0x001C    | WO     |
| SHA_START_REG                              | Starts the SHA accelerator for Typical SHA operation                                             | 0x0010    | WO     |
| SHA_DMA_CONTINUE_REG                      | Continues SHA operation (only effective in DMA-SHA mode)                                         | 0x0020    | WO     |
| SHA_DMA_BLOCK_NUM_REG                     | Block number register (only effective in DMA-SHA mode)                                           | 0x000C    | R/W    |
| **Status Registers**                      |                                                                                                  |           |        |
| SHA_BUSY_REG                              | Represents if SHA Accelerator is busy or not                                                   | 0x0018    | RO     |
| **Interrupt Registers**                   |                                                                                                  |           |        |
| SHA_INT_CLEAR_REG                         | DMA-SHA interrupt clear register                                                                | 0x0024    | WO     |
| SHA_INT_ENA_REG                            | DMA-SHA interrupt enable register                                                               | 0x0028    | R/W    |
| **Data Registers**                        |                                                                                                  |           |        |
| SHA_H_0_REG                               | Hash value                                                                                       | 0x0040    | R/W    |
| SHA_H_1_REG                               | Hash value                                                                                       | 0x0044    | R/W    |
| SHA_H_2_REG                               | Hash value                                                                                       | 0x0048    | R/W    |
| SHA_H_3_REG                               | Hash value                                                                                       | 0x004C    | R/W    |
| SHA_H_4_REG                               | Hash value                                                                                       | 0x0050    | R/W    |
| SHA_H_5_REG                               | Hash value                                                                                       | 0x0054    | R/W    |
| SHA_H_6_REG                               | Hash value                                                                                       | 0x0058    | R/W    |
| SHA_H_7_REG                               | Hash value                                                                                       | 0x005C    | R/W    |
| SHA_H_8_REG                               | Hash value                                                                                       | 0x0060    | R/W    |
| SHA_H_9_REG                               | Hash value                                                                                       | 0x0064    | R/W    |
| SHA_H_10_REG                              | Hash value                                                                                       | 0x0068    | R/W    |
| SHA_H_11_REG                              | Hash value                                                                                       | 0x006C    | R/W    |
| SHA_H_12_REG                              | Hash value                                                                                       | 0x0070    | R/W    |
| SHA_H_13_REG                              | Hash value                                                                                       | 0x0074    | R/W    |
| SHA_H_14_REG                              | Hash value                                                                                       | 0x0078    | R/W    |
| SHA_H_15_REG                              | Hash value                                                                                       | 0x007C    | R/W    |
| SHA_M_0_REG                               | Message                                                                                          | 0x0080    | R/W    |
| SHA_M_1_REG                               | Message                                                                                          | 0x0084    | R/W    |
| SHA_M_2_REG                               | Message                                                                                          | 0x0088    | R/W    |
| SHA_M_3_REG                               | Message                                                                                          | 0x008C    | R/W    |
| SHA_M_4_REG                               | Message                                                                                          | 0x0090    | R/W    |
| SHA_M_5_REG                               | Message                                                                                          | 0x0094    | R/W    |
```