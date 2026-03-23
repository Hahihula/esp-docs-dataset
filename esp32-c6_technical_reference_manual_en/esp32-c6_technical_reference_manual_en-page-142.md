

```markdown
| Name                                       | Description                                                                                   | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------------------------|-----------|--------|
| GDMA_IN_LINK_CHO_REG                      | Linked list descriptor configuration and control register of RX channel 0                     | 0x0080    | varies |
| GDMA_OUT_CONFO_CHO_REG                    | Configuration register 0 of TX channel 0                                                   | 0x00D0    | R/W    |
| GDMA_OUT_CONF1_CHO_REG                    | Configuration register 1 of TX channel 0                                                  | 0x00D4    | R/W    |
| GDMA_OUT_PUSH_CHO_REG                     | Push control register of RX channel 0                                                      | 0x00DC    | varies |
| GDMA_OUT_LINK_CHO_REG                     | Linked list descriptor configuration and control register of TX channel 0                   | 0x00E0    | varies |
| GDMA_IN_CONFO_CH1_REG                     | Configuration register 0 of RX channel 1                                                  | 0x0130    | R/W    |
| GDMA_IN_CONF1_CH1_REG                     | Configuration register 1 of RX channel 1                                                  | 0x0134    | R/W    |
| GDMA_IN_POP_CH1_REG                       | Pop control register of RX channel 1                                                       | 0x013C    | varies |
| GDMA_IN_LINK_CH1_REG                      | Linked list descriptor configuration and control register of RX channel 1                   | 0x0140    | varies |
| GDMA_OUT_CONFO_CH1_REG                    | Configuration register 0 of TX channel 1                                                  | 0x0190    | R/W    |
| GDMA_OUT_CONF1_CH1_REG                    | Configuration register 1 of TX channel 1                                                  | 0x0194    | R/W    |
| GDMA_OUT_PUSH_CH1_REG                     | Push control register of RX channel 1                                                      | 0x019C    | varies |
| GDMA_OUT_LINK_CH1_REG                     | Linked list descriptor configuration and control register of TX channel 1                   | 0x01A0    | varies |
| GDMA_IN_CONFO_CH2_REG                     | Configuration register 0 of RX channel 2                                                  | 0x01F0    | R/W    |
| GDMA_IN_CONF1_CH2_REG                     | Configuration register 1 of RX channel 2                                                  | 0x01F4    | R/W    |
| GDMA_IN_POP_CH2_REG                       | Pop control register of RX channel 2                                                       | 0x01FC    | varies |
| GDMA_IN_LINK_CH2_REG                      | Linked list descriptor configuration and control register of RX channel 2                   | 0x0200    | varies |
| GDMA_OUT_CONFO_CH2_REG                    | Configuration register 0 of TX channel 2                                                  | 0x0250    | R/W    |
| GDMA_OUT_CONF1_CH2_REG                    | Configuration register 1 of TX channel 2                                                  | 0x0254    | R/W    |
| GDMA_OUT_PUSH_CH2_REG                     | Push control register of RX channel 2                                                      | 0x025C    | varies |
| GDMA_OUT_LINK_CH2_REG                     | Linked list descriptor configuration and control register of TX channel 2                   | 0x0260    | varies |

**Version Register**

| Name               | Description       | Address   | Access |
|--------------------|-------------------|-----------|--------|
| GDMA_DATE_REG      | Version control register | 0x0068    | R/W    |

**Status Registers**

| Name                                       | Description                                                                                   | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------------------------|-----------|--------|
| GDMA_INFIFO_STATUS_CHO_REG                | Receive FIFO status of RX channel 0                                                           | 0x0078    | RO     |
| GDMA_IN_STATE_CHO_REG                     | Receive status of RX channel 0                                                                | 0x0084    | RO     |
| GDMA_IN_SUC_EOF_DES_ADDR_CHO_REG          | Receive descriptor address when EOF occurs on RX channel 0                                   | 0x0088    | RO     |
| GDMA_IN_ERR_EOF_DES_ADDR_CHO_REG          | Receive descriptor address when errors occur of RX channel 0                                 | 0x008C    | RO     |
| GDMA_IN_DSCR_CHO_REG                      | Address of the next receive descriptor pointed by the current pre-read receive descriptor on RX channel 0 | 0x0090    | RO     |
| GDMA_IN_DSCR_BFO_CHO_REG                  | Address of the current pre-read receive descriptor on RX channel 0                           | 0x0094    | RO     |
```