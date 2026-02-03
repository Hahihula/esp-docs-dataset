**Chapter 3: DMA Controller (DMA)**

---

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| GDMA_IN_SUC_EOFDES_ADDR_CH4\_\_REG | Inlink descriptor address when EOF occurs of RX channel 4 | 0x0328 | RO |
| GDMA_IN_ERR_EOFDES_ADDR_CH4\_\_REG | Inlink descriptor address when errors occur of RX channel 4 | 0x032C | RO |
| GDMA_IN_DSCR_CH4\_REG | Address of the next receive descriptor pointed by the current pre-read receive descriptor on RX channel 4 | 0x0330 | RO |
| GDMA_IN_DSCR_BFO\_CH4\_REG | Address of the current pre-read receive descriptor on RX channel 4 | 0x0334 | RO |
| GDMA_IN_DSCR_BF1\_CH4\_REG | Address of the previous pre-read receive descriptor on RX channel 4 | 0x0338 | RO |
| GDMA_OUTFIFO\_STATUS\_CH4\_REG | Transmit FIFO status of TX channel 4 | 0x0378 | RO |
| GDMA_OUT_STATE\_CH4\_REG | Transmit status of TX channel 4 | 0x0384 | RO |
| GDMA_OUT_EOFDES_ADDR_CH4\_REG | Outlink descriptor address when EOF occurs of TX channel 4 | 0x0388 | RO |
| GDMA_OUT_EOFBFRDES_ADDR_CH4\_\_REG | The last outlink descriptor address when EOF occurs of TX channel 4 | 0x038C | RO |
| GDMA_OUT_DSCR\_CH4\_REG | Address of the next transmit descriptor pointed by the current pre-transmit descriptor on TX channel 4 | 0x0390 | RO |
| GDMA_OUT_DSCR_BFO\_CH4\_REG | Address of the current pre-transmit descriptor on TX channel 4 | 0x0394 | RO |
| GDMA_OUT_DSCR_BF1\_CH4\_REG | Address of the previous pre-transmit descriptor on TX channel 4 | 0x0398 | RO |

---

**Priority Registers**

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| GDMA_INPRI\_CHO\_REG | Priority register of RX channel 0 | 0x0044 | R/W |
| GDMA_INPRI\_CHO\_REG | Priority register of TX channel 0 | 0x00A4 | R/W |
| GDMA_INPRI\_CH1\_REG | Priority register of RX channel 1 | 0x0104 | R/W |
| GDMA_INPRI\_CH1\_REG | Priority register of TX channel 1 | 0x0164 | R/W |
| GDMA_INPRI\_CH2\_REG | Priority register of RX channel 2 | 0x01C4 | R/W |
| GDMA_INPRI\_CH2\_REG | Priority register of TX channel 2 | 0x0224 | R/W |
| GDMA_INPRI\_CH3\_REG | Priority register of RX channel 3 | 0x0284 | R/W |
| GDMA_OUTPRI\_CH3\_REG | Priority register of TX channel 3 | 0x02E4 | R/W |
| GDMA_INPRI\_CH4\_REG | Priority register of RX channel 4 | 0x0344 | R/W |
| GDMA_OUTPRI\_CH4\_REG | Priority register of TX channel 4 | 0x03A4 | R/W |

---

**Peripheral Selection Registers**

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| GDMA_INPERI\_SEL\_CHO\_REG | Peripheral selection of RX channel 0 | 0x0048 | R/W |
| GDMA_OUTPERI\_SEL\_CHO\_REG | Peripheral selection of TX channel 0 | 0x00A8 | R/W |
| GDMA_INPERI\_SEL\_CH1\_REG | Peripheral selection of RX channel 1 | 0x0108 | R/W |
| GDMA_OUTPERI\_SEL\_CH1\_REG | Peripheral selection of TX channel 1 | 0x0168 | R/W |
| GDMA_INPERI\_SEL\_CH2\_REG | Peripheral selection of RX channel 2 | 0x01C8 | R/W |
| GDMA_OUTPERI\_SEL\_CH2\_REG | Peripheral selection of TX channel 2 | 0x0228 | R/W |
| GDMA_INPERI\_SEL\_CH3\_REG | Peripheral selection of RX channel 3 | 0x0288 | R/W |
| GDMA_OUTPERI\_SEL\_CH3\_REG | Peripheral selection of TX channel 3 | 0x02E8 | R/W |

---

*Espressif Systems*

*Submit Documentation Feedback*

**ESP32-S3 TRM (Version 1.7)**

GoBack