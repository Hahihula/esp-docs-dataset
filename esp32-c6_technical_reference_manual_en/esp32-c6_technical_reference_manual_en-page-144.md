

```markdown
| Name                                       | Description                                                                                      | Address | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|---------|--------|
| GDMA_IN_SUC_EOF_DES_ADDR_CH2_REG           | Receive descriptor address when EOF occurs on RX channel 2                                        | 0x0208  | RO     |
| GDMA_IN_ERR_EOF_DES_ADDR_CH2_REG           | Receive descriptor address when errors occur of RX channel 2                                      | 0x020C  | RO     |
| GDMA_IN_DSCR_CH2_REG                       | Address of the next receive descriptor pointed by the current pre-read receive descriptor on RX channel 2 | 0x0210  | RO     |
| GDMA_IN_DSCR_BFO_CH2_REG                   | Address of the current pre-read receive descriptor on RX channel 2                               | 0x0214  | RO     |
| GDMA_IN_DSCR_BF1_CH2_REG                   | Address of the previous pre-read receive descriptor on RX channel 2                              | 0x0218  | RO     |
| GDMA_OUTFIFO_STATUS_CH2_REG                | Transmit FIFO status of TX channel 2                                                            | 0x0258  | RO     |
| GDMA_OUT_STATE_CH2_REG                     | Transmit status of TX channel 2                                                                 | 0x0264  | RO     |
| GDMA_OUT_EOF_DES_ADDR_CH2_REG              | Transmit descriptor address when EOF occurs on TX channel 2                                       | 0x0268  | RO     |
| GDMA_OUT_EOF_BFR_DES_ADDR_CH2_REG          | The last transmit descriptor address when EOF occurs on TX channel 2                             | 0x026C  | RO     |
| GDMA_OUT_DSCR_CH2_REG                      | Address of the next transmit descriptor pointed by the current pre-read transmit descriptor on TX channel 2 | 0x0270  | RO     |
| GDMA_OUT_DSCR_BFO_CH2_REG                  | Address of the current pre-read transmit descriptor on TX channel 2                              | 0x0274  | RO     |
| GDMA_OUT_DSCR_BF1_CH2_REG                  | Address of the previous pre-read transmit descriptor on TX channel 2                             | 0x0278  | RO     |

Priority Registers
| Name                                       | Description                                                                                      | Address | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|---------|--------|
| GDMA_IN_PRI_CHO_REG                        | Priority register of RX channel 0                                                                | 0x009C  | R/W    |
| GDMA_OUT_PRI_CHO_REG                       | Priority register of TX channel 0                                                                | 0x00FC  | R/W    |
| GDMA_IN_PRI_CH1_REG                        | Priority register of RX channel 1                                                                | 0x015C  | R/W    |
| GDMA_OUT_PRI_CH1_REG                       | Priority register of TX channel 1                                                                | 0x01BC  | R/W    |
| GDMA_IN_PRI_CH2_REG                        | Priority register of RX channel 2                                                                | 0x021C  | R/W    |
| GDMA_OUT_PRI_CH2_REG                       | Priority register of TX channel 2                                                                | 0x027C  | R/W    |

Peripheral Selection Registers
| Name                                       | Description                                                                                      | Address | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|---------|--------|
| GDMA_IN_PERI_SEL_CHO_REG                   | Peripheral selection register of RX channel 0                                                   | 0x00AO  | R/W    |
| GDMA_OUT_PERI_SEL_CHO_REG                  | Peripheral selection register of TX channel 0                                                   | 0x0100  | R/W    |
| GDMA_IN_PERI_SEL_CH1_REG                   | Peripheral selection register of RX channel 1                                                   | 0x0160  | R/W    |
| GDMA_OUT_PERI_SEL_CH1_REG                  | Peripheral selection register of TX channel 1                                                   | 0x01C0  | R/W    |
| GDMA_IN_PERI_SEL_CH2_REG                   | Peripheral selection register of RX channel 2                                                   | 0x0220  | R/W    |
| GDMA_OUT_PERI_SEL_CH2_REG                  | Peripheral selection register of TX channel 2                                                   | 0x0280  | R/W    |
```