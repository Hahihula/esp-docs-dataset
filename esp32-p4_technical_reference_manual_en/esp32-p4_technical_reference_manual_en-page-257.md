
```markdown
| Name                                       | Description                                                                                      | Address | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|---------|--------|
| AXI_DMA_TX_CRC_DATA_EN_WR_DATA_CH2_REG    | TX channel 2 CRC data input mask target register                                                | 0x0268  | R/W    |
| AXI_DMA_TX_CRC_DATA_EN_ADDR_CH2_REG       | TX channel 2 CRC data input mask target register                                                | 0x026C  | R/W    |
| AXI_DMA_ARB_TIMEOUT_REG                    | Arbitration timeout configuration register                                                     | 0x0270  | R/W    |
| AXI_DMA_WEIGHT_EN_REG                      | Weight arbitration enable register                                                             | 0x0274  | R/W    |
| AXI_DMA_IN_MEM_CONF_REG                    | Internal memory power configuration register for RX channel                                    | 0x0278  | R/W    |
| AXI_DMA_INTR_MEM_START_ADDR_REG            | Accessible internal memory start address configuration register                                | 0x027C  | R/W    |
| AXI_DMA_INTR_MEM_END_ADDR_REG              | Accessible internal memory end address configuration register                                  | 0x0280  | R/W    |
| AXI_DMA_EXTR_MEM_START_ADDR_REG            | Accessible external memory start address configuration register                                | 0x0284  | R/W    |
| AXI_DMA_EXTR_MEM_END_ADDR_REG              | Accessible external memory end address configuration register                                  | 0x0288  | R/W    |
| AXI_DMA_MISC_CONF_REG                      | Miscellaneous register                                                                         | 0x02A8  | R/W    |
| AXI_DMA_LINK_SWITCH_STATE_REG              | Linked list switching configuration register                                                   | 0x02DC  | R/W    |
| AXI_DMA_RX_CRC_EN_WR_DATA_CH0_REG          | CRC RX channel 0 CRC intermediate result mask register                                         | 0x0058  | R/W    |
| AXI_DMA_RX_CRC_EN_WR_DATA_CH1_REG          | CRC RX channel 1 CRC intermediate result mask register                                         | 0x00C0  | R/W    |
| AXI_DMA_RX_CRC_EN_WR_DATA_CH2_REG          | CRC RX channel 2 CRC intermediate result mask register                                         | 0x0128  | R/W    |

Status Registers
| Name                                       | Description                                                                                      | Address | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|---------|--------|
| AXI_DMA_INFIFO_STATUS_CHO_REG              | RX channel 0 FIFO status register                                                               | 0x0018  | RO     |
| AXI_DMA_IN_STATE_CHO_REG                   | RX channel 0 status register                                                                    | 0x0028  | RO     |
| AXI_DMA_IN_SUC_EOF_DES_ADDR_CHO_REG        | Receive descriptor address when EOF occurs on RX channel 0                                       | 0x002C  | RO     |
| AXI_DMA_IN_ERR_EOF_DES_ADDR_CHO_REG        | Receive descriptor address when errors occur on RX channel 0                                    | 0x0030  | RO     |
| AXI_DMA_IN_DSCR_CHO_REG                    | Address of the next receive descriptor pointed by the current pre-read receive descriptor on RX channel 0 | 0x0034  | RO     |
| AXI_DMA_IN_DSCR_BFO_CHO_REG                | Address of the current pre-read receive descriptor on RX channel 0                              | 0x0038  | RO     |
| AXI_DMA_IN_DSCR_BF1_CHO_REG                | Address of the previous pre-read receive descriptor on RX channel 0                             | 0x003C  | RO     |
| AXI_DMA_INFIFO_STATUS_CH1_REG              | RX channel 1 FIFO status register                                                               | 0x0080  | RO     |
| AXI_DMA_IN_STATE_CH1_REG                   | RX channel 1 status register                                                                    | 0x0090  | RO     |
| AXI_DMA_IN_SUC_EOF_DES_ADDR_CH1_REG        | Receive descriptor address when EOF occurs on RX channel 1                                       | 0x0094  | RO     |
| AXI_DMA_IN_ERR_EOF_DES_ADDR_CH1_REG        | Receive descriptor address when errors occur on RX channel 1                                    | 0x0098  | RO     |
```