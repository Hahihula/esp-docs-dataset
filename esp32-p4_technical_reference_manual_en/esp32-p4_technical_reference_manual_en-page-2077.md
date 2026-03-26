

```markdown
| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| CSI_HOST_INT_ST_BNDRY_FRAME_FATAL_REG      | Frame boundary fatal interrupt status register                              | 0x0280  | RC     |
| CSI_HOST_INT_MSK_BNDRY_FRAME_FATAL_REG     | Frame boundary fatal interrupt mask register                                | 0x0284  | R/W    |
| CSI_HOST_INT_FORCE_BNDRY_FRAME_FATAL_REG   | Frame boundary fatal interrupt force register                               | 0x0288  | R/W    |
| CSI_HOST_INT_ST_SEQ_FRAME_FATAL_REG        | Frame sequence fatal interrupt status register                              | 0x0290  | RC     |
| CSI_HOST_INT_MSK_SEQ_FRAME_FATAL_REG       | Frame sequence fatal interrupt mask register                                | 0x0294  | R/W    |
| CSI_HOST_INT_FORCE_SEQ_FRAME_FATAL_REG     | Frame sequence fatal interrupt force register                               | 0x0298  | R/W    |
| CSI_HOST_INT_ST_CRC_FRAME_FATAL_REG        | Frame CRC fatal interrupt status register                                   | 0x02A0  | RC     |
| CSI_HOST_INT_MSK_CRC_FRAME_FATAL_REG       | Frame CRC fatal interrupt mask register                                    | 0x02A4  | R/W    |
| CSI_HOST_INT_FORCE_CRC_FRAME_FATAL_REG     | Frame CRC fatal interrupt force register                                   | 0x02A8  | R/W    |
| CSI_HOST_INT_ST_PLD_CRC_FATAL_REG          | Payload CRC fatal interrupt status register                                 | 0x02B0  | RC     |
| CSI_HOST_INT_MSK_PLD_CRC_FATAL_REG         | Payload CRC fatal interrupt mask register                                  | 0x02B4  | R/W    |
| CSI_HOST_INT_FORCE_PLD_CRC_FATAL_REG       | Payload CRC fatal interrupt force register                                 | 0x02B8  | R/W    |
| CSI_HOST_INT_ST_DATA_ID_REG                | Data ID interrupt status register                                          | 0x02C0  | RC     |
| CSI_HOST_INT_MSK_DATA_ID_REG               | Data ID interrupt mask register                                            | 0x02C4  | R/W    |
| CSI_HOST_INT_FORCE_DATA_ID_REG             | Data ID interrupt force register                                           | 0x02C8  | R/W    |
| CSI_HOST_INT_ST_ECC_CORRECTED_REG          | Header error detected and corrected interrupt status register               | 0x02D0  | RC     |
| CSI_HOST_INT_MSK_ECC_CORRECTED_REG         | Header error detected and corrected interrupt mask register                 | 0x02D4  | R/W    |
| CSI_HOST_INT_FORCE_ECC_CORRECTED_REG       | Header error detected and corrected interrupt force register                | 0x02D8  | R/W    |

**Status Register**

| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| CSI_HOST_PHY_STOPSTATE_REG                 | RX D-PHY stop state signal status register                                 | 0x004C  | RO     |
```