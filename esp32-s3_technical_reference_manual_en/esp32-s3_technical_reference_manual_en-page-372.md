**Chapter 3: GDMA Controller (GDMA)**

---

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| **GDMA_OUT_DSCR_CHO_REG** | Address of the next transmit descriptor pointed by the current pre-read transmit descriptor on TX channel 0 | `0x0090` | RO |
| **GDMA_OUT_DSCR_BFO_CHO_REG** | Address of the current pre-read transmit descriptor on TX channel 0 | `0x0094` | RO |
| **GDMA_OUT_DSCR_BF1_CHO_REG** | Address of the previous pre-read transmit descriptor on TX channel 0 | `0x0098` | RO |
| **GDMA_INFIFO_STATUS_CH1_REG** | Receive FIFO status of RX channel 1 | `0x00D8` | RO |
| **GDMA_IN_STATE_CH1_REG** | Receive status of RX channel 1 | `0x00E4` | RO |
| **GDMA_IN_SUC_EOFDES_ADDR_CH1_REG** | Inlink descriptor address when EOF occurs of RX channel 1 | `0x00E8` | RO |
| **GDMA_IN_ERR_EOFDES_ADDR_CH1_REG** | Inlink descriptor address when errors occur of RX channel 1 | `0x00EC` | RO |
| **GDMA_IN_DSCR_CH1_REG** | Address of the next receive descriptor pointed by the current pre-read receive descriptor on RX channel 1 | `0x00F0` | RO |
| **GDMA_IN_DSCR_BFO_CH1_REG** | Address of the current pre-read receive descriptor on RX channel 1 | `0x00F4` | RO |
| **GDMA_IN_DSCR_BF1_CH1_REG** | Address of the previous pre-read receive descriptor on RX channel 1 | `0x00F8` | RO |
| **GDMA_OUTFIFO_STATUS_CH1_REG** | Transmit FIFO status of TX channel 1 | `0x0138` | RO |
| **GDMA_OUT_STATE_CH1_REG** | Transmit status of TX channel 1 | `0x0144` | RO |
| **GDMA_OUT_EOFDES_ADDR_CH1_REG** | Outlink descriptor address when EOF occurs of TX channel 1 | `0x0148` | RO |
| **GDMA_OUT_EOF_BFRDES_ADDR_CH1_REG** | The last outlink descriptor address when EOF occurs of TX channel 1 | `0x014C` | RO |
| **GDMA_OUT_DSCR_CH1_REG** | Address of the next transmit descriptor pointed by the current pre-read transmit descriptor on TX channel 1 | `0x0150` | RO |
| **GDMA_OUT_DSCR_BFO_CH1_REG** | Address of the current pre-read transmit descriptor on RX channel 1 | `0x0154` | RO |
| **GDMA_OUT_DSCR_BF1_CH1_REG** | Address of the previous pre-read transmit descriptor on TX channel 1 | `0x0158` | RO |
| **GDMA_INFIFO_STATUS_CH2_REG** | Receive FIFO status of RX channel 2 | `0x0198` | RO |
| **GDMA_IN_STATE_CH2_REG** | Receive status of RX channel 2 | `0x01A4` | RO |
| **GDMA_IN_SUC_EOFDES_ADDR_CH2_REG** | Inlink descriptor address when EOF occurs of RX channel 2 | `0x01A8` | RO |
| **GDMA_IN_ERR_EOFDES_ADDR_CH2_REG** | Inlink descriptor address when errors occur of RX channel 2 | `0x01AC` | RO |
| **GDMA_IN_DSCR_CH2_REG** | Address of the next receive descriptor pointed by the current pre-read receive descriptor on RX channel 2 | `0x01B0` | RO |
| **GDMA_IN_DSCR_BFO_CH2_REG** | Address of the current pre-read receive descriptor on RX channel 2 | `0x01B4` | RO |

---

*Espressif Systems*

*Page: 372 ESP32-S3 TRM (Version 1.7)*

*Submit Documentation Feedback*