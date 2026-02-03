**Chapter 3: GDMA Controller (GDMA)**

---

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| **GDMA_IN_DSCR_BF1_CH2_REG** | Address of the previous pre-read receive descriptor on RX channel 2 | `0x01B8` | RO |
| **GDMA_OUTFIFO_STATUS_CH2_REG** | Transmit FIFO status of TX channel 2 | `0x01F8` | RO |
| **GDMA_OUT_STATE_CH2_REG** | Transmit status of TX channel 2 | `0x0204` | RO |
| **GDMA_OUT_EOFDES_ADDR_CH2_REG** | Outlink descriptor address when EOF occurs of TX channel 2 | `0x0208` | RO |
| **GDMA_OUT_EOFBFR_DES_ADDR_CH2_REG** | The last outlink descriptor address when EOF occurs of TX channel 2 | `0x020C` | RO |
| **GDMA_OUT_DSCR_CH2_REG** | Address of the next transmit descriptor pointed by the current pre-read transmit descriptor on TX channel 2 | `0x0210` | RO |
| **GDMA_OUT_DSCR_BFO_CH2_REG** | Address of the current pre-read transmit descriptor on TX channel 2 | `0x0214` | RO |
| **GDMA_OUT_DSCR_BF1_CH2_REG** | Address of the previous pre-read transmit descriptor on TX channel 2 | `0x0218` | RO |
| **GDMA_INFIFO_STATUS_CH3_REG** | Receive FIFO status of RX channel 3 | `0x0258` | RO |
| **GDMA_IN_STATE_CH3_REG** | Receive status of RX channel 3 | `0x0264` | RO |
| **GDMA_IN_SUC_EOFDES_ADDR_CH3_REG** | Inlink descriptor address when EOF occurs of RX channel 3 | `0x0268` | RO |
| **GDMA_IN_ERR_EOFDES_ADDR_CH3_REG** | Inlink descriptor address when errors occur of RX channel 3 | `0x026C` | RO |
| **GDMA_IN_DSCR_CH3_REG** | Address of the next receive descriptor pointed by the current pre-read receive descriptor on RX channel 3 | `0x0270` | RO |
| **GDMA_IN_DSCR_BFO_CH3_REG** | Address of the current pre-read receive descriptor on RX channel 3 | `0x0274` | RO |
| **GDMA_IN_DSCR_BF1_CH3_REG** | Address of the previous pre-read receive descriptor on RX channel 3 | `0x0278` | RO |
| **GDMA_OUTFIFO_STATUS_CH3_REG** | Transmit FIFO status of TX channel 3 | `0x02B8` | RO |
| **GDMA_OUT_STATE_CH3_REG** | Transmit status of TX channel 3 | `0x02C4` | RO |
| **GDMA_OUT_EOFDES_ADDRCH3_REG** | Outlink descriptor address when EOF occurs of TX channel 3 | `0x02C8` | RO |
| **GDMA_OUT_EOFBFR_DES_ADDR_CH3_REG** | The next transmit descriptor pointed by the current pre-read transmit descriptor on TX channel 3 | `0x02CC` | RO |
| **GDMA_OUT_DSCR_CH3_REG** | Address of the previous pre-read transmit descriptor on TX channel 3 | `0x02D0` | RO |
| **GDMA_OUT_DSCR_BFO_CH3_REG** | Address of the current pre-read transmit descriptor on TX channel 3 | `0x02D4` | RO |
| **GDMA_OUT_DSCR_BF1_CH3_REG** | Address of the previous pre-read transmit descriptor on TX channel 3 | `0x02D8` | RO |
| **GDMA_INFIFO_STATUS_CH4_REG** | Receive FIFO status of RX channel 4 | `0x0318` | RO |
| **GDMA_IN_STATE_CH4_REG** | Receive status of RX channel 4 | `0x0324` | RO |

---

*Espressif Systems*

*Submit Documentation Feedback*

*ESP32-S3 TRM (Version 1.7)*

---