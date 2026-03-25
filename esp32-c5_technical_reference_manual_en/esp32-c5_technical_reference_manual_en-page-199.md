

```markdown
| Name                                       | Description                                                                                      | Address | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|---------|--------|
| AHB_DMA_IN_LINK_ADDR_CH2_REG              | Linked list descriptor configuration register of RX channel 2                                    | 0x03B4  | R/W    |
| AHB_DMA_OUT_LINK_ADDR_CHO_REG             | Linked list descriptor configuration register of TX channel 0                                   | 0x03B8  | R/W    |
| AHB_DMA_OUT_LINK_ADDR_CH1_REG             | Linked list descriptor configuration register of TX channel 1                                   | 0x03BC  | R/W    |
| AHB_DMA_OUT_LINK_ADDR_CH2_REG             | Linked list descriptor configuration register of TX channel 2                                   | 0x03C0  | R/W    |
| AHB_DMA_INTR_MEM_START_ADDR_REG           | Accessible address space start address configuration register                                   | 0x03C4  | R/W    |
| AHB_DMA_INTR_MEM_END_ADDR_REG             | Accessible address space end address configuration register                                    | 0x03C8  | R/W    |
| AHB_DMA_ARB_TIMEOUT_REG                   | Weight arbitration timeout configuration register                                              | 0x03DC  | R/W    |
| AHB_DMA_WEIGHT_EN_REG                     | Weight arbitration enable register                                                             | 0x0400  | R/W    |
| AHB_DMA_MODULE_CLK_EN_REG                 | Force clock enable register for all internal GDMA modules                                       | 0x0404  | R/W    |
| Version Registers                         |                                                |         |        |
| AHB_DMA_DATE_REG                          | Version control register                                                                       | 0x0068  | R/W    |
| Status Registers                          |                                                |         |        |
| AHB_DMA_INFIFO_STATUS_CHO_REG             | RX channel 0 FIFO status                                                                        | 0x0078  | RO     |
| AHB_DMA_IN_STATE_CHO_REG                  | RX channel 0 status                                                                             | 0x0084  | RO     |
| AHB_DMA_IN_SUC_EOF_DES_ADDR_CHO_REG       | Receive descriptor address when EOF occurs on RX channel 0                                       | 0x0088  | RO     |
| AHB_DMA_IN_ERR_EOF_DES_ADDR_CHO_REG       | Receive descriptor address when errors occur on RX channel 0                                     | 0x008C  | RO     |
| AHB_DMA_IN_DSCR_CHO_REG                   | Address of the next receive descriptor pointed by the current pre-read receive descriptor on RX channel 0 | 0x0090  | RO     |
| AHB_DMA_IN_DSCR_BFO_CHO_REG               | Address of the current pre-read receive descriptor on RX channel 0                               | 0x0094  | RO     |
```