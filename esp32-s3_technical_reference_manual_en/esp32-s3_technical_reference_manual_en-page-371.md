**Chapter 3: GDMA Controller (GDMA)**

---

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| **Interrupt Control and Status Registers** | | | |
| GDMA_IN_INT_ENA_CH3_REG | Interrupt enable bits of RX channel 3 | 0x0250 | R/W |
| GDMA_IN_INT_CLR_CH3_REG | Interrupt clear bits of RX channel 3 | 0x0254 | WT |
| GDMA_OUT_INT_RAW_CH3_REG | Raw status interrupt of TX channel 3 | 0x02A8 | R/WTC/SS |
| GDMA_OUT_INT_ST_CH3_REG | Masked interrupt of TX channel 3 | 0x02AC | RO |
| GDMA_OUT_INT_ENA_CH3_REG | Interrupt enable bits of TX channel 3 | 0x02B0 | R/W |
| GDMA_OUT_INT_CLR_CH3_REG | Interrupt clear bits of TX channel 3 | 0x02B4 | WT |
| GDMA_IN_INT_RAW_CH4_REG | Raw status interrupt of RX channel 4 | 0x0308 | R/WTC/SS |
| GDMA_IN_INT_ST_CH4_REG | Masked interrupt of RX channel 4 | 0x030C | RO |
| GDMA_OUT_INT_ENA_CH4_REG | Interrupt enable bits of RX channel 4 | 0x0310 | R/W |
| GDMA_OUT_INT_CLR_CH4_REG | Interrupt clear bits of RX channel 4 | 0x0314 | WT |
| GDMA_OUT_INT_RAW_CH4_REG | Raw status interrupt of TX channel 4 | 0x0368 | R/WTC/SS |
| GDMA_OUT_INT_ST_CH4_REG | Masked interrupt of TX channel 4 | 0x036C | RO |
| GDMA_IN_INT_ENA_CH4_REG | Interrupt enable bits of TX channel 4 | 0x0370 | R/W |
| GDMA_OUT_INT_CLR_CH4_REG | Interrupt clear bits of TX channel 4 | 0x0374 | WT |
| **Interrupt Control and Status Registers** | | | |
| GDMA_EXTMEM_REJECT_INT_RAW_REG | Raw interrupt status of external RAM permission | 0x03FC | R/WTC/SS |
| GDMA_EXTMEM_REJECT_INT_ST_REG | Masked interrupt status of external RAM permission | 0x0400 | RO |
| GDMA_EXTMEM_REJECT_INT_ENA_REG | Interrupt enable bits of external RAM permission | 0x0404 | R/W |
| GDMA_EXTMEM_REJECT_INT_CLR_REG | Interrupt clear bits of external RAM permission | 0x0408 | WT |
| **Status Registers** | | | |
| GDMA_INFIFO_STATUS_CHO_REG | Receive FIFO status of RX channel 0 | 0x0018 | RO |
| GDMA_IN_STATE_CHO_REG | Receive status of RX channel 0 | 0x0024 | RO |
| GDMA_IN_SUC_EOFDES_ADDR_CHO_REG | Inlink descriptor address when EOF occurs of RX channel 0 | 0x0028 | RO |
| GDMA_IN_ERR_EOFDES_ADDR_CHO_REG | Inlink descriptor address when errors occur of RX channel 0 | 0x002C | RO |
| GDMA_IN_DSCR_CHO_REG | Address of the next receive descriptor pointed by the current pre-read receive descriptor on RX channel 0 | 0x0030 | RO |
| GDMA_IN_DSCR_BFO_CHO_REG | Address of the current pre-read receive descriptor on RX channel 0 | 0x0034 | RO |
| GDMA_IN_DSCR_BF1_CHO_REG | Address of the previous pre-read receive descriptor on RX channel 0 | 0x0038 | RO |
| GDMA_OUTFIFO_STATUS_CHO_REG | Transmit FIFO status of TX channel 0 | 0x0078 | RO |
| GDMA_OUT_STATE_CHO_REG | Transmit status of TX channel 0 | 0x0084 | RO |
| GDMA_OUT_EOFDES_ADDR_CHO_REG | Outlink descriptor address when EOF occurs of TX channel 0 | 0x0088 | RO |
| GDMA_OUT_EOFBFRDES_ADDR_CHO_REG | The last outlink descriptor address when EOF occurs of TX channel 0 | 0x008C | RO |

---

*Espressif Systems*

*Page: 371 ESP32-S3 TRM (Version 1.7)*

*Submit Documentation Feedback*