**Chapter 3: GDMA Controller (GDMA)**

---

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| **Configuration Registers and Control Registers for RX Channel 4** | | | |
| GDMA_OUT_CONF1_CH3_REG | Configuration register 1 of TX channel 3 | 0x02A4 | R/W |
| GDMA_OUT_PUSH_CH3_REG | Push control register of RX channel 3 | 0x02BC | varies |
| GDMA_OUT_LINK_CH3_REG | Link descriptor configuration and control register of TX channel 3 | 0x02CO | varies |
| GDMA_IN_CONF0_CH4_REG | Configuration register O of RX channel 4 | 0x0300 | R/W |
| GDMA_IN_CONF1_CH4_REG | Configuration register 1 of RX channel 4 | 0x0304 | R/W |
| GDMA_IN_POP_CH4_REG | Pop control register of RX channel 4 | 0x031C | varies |
| GDMA_IN_LINK_CH4_REG | Link descriptor configuration and control register of RX channel 4 | 0x0320 | varies |
| GDMA_OUT_CONF0_CH4_REG | Configuration register O of TX channel 4 | 0x0360 | R/W |
| GDMA_OUT_CONF1_CH4_REG | Configuration register 1 of TX channel 4 | 0x0364 | R/W |
| GDMA_OUT_PUSH_CH4_REG | Push control register of RX channel 4 | 0x037C | varies |
| GDMA_OUT_LINK_CH4_REG | Link descriptor configuration and control register of TX channel 4 | 0x0380 | varies |
| **Interrupt Registers** | | | |
| GDMA_PD_CONF_REG | reserved | 0x03C4 | R/W |
| GDMA_MISC_CONF_REG | Miscellaneous register | 0x03C8 | R/W |
| **Interrupt Status and Enable Registers for RX Channel 0 to 2, TX Channel 1** | | | |
| GDMA_IN_INT_RAW_CHO_REG | Raw status interrupt of RX channel O | 0x0008 | R/WTC/SS |
| GDMA_IN_INT_ST_CHO_REG | Masked interrupt bits of RX channel O | 0x000C | RO |
| GDMA_IN_INT_ENA_CHO_REG | Interrupt enable bits of RX channel O | 0x0010 | R/W |
| GDMA_IN_INT_CLR_CHO_REG | Interrupt clear bits of RX channel O | 0x0014 | WT |
| GDMA_OUT_INT_RAW_CHO_REG | Raw status interrupt TX channel O | 0x0068 | R/WTC/SS |
| GDMA_OUT_INT_ST_CHO_REG | Masked interrupt bits of TX channel O | 0x00C6 | RO |
| GDMA_OUT_INT_ENA_CHO_REG | Interrupt enable bits of TX channel O | 0x0070 | R/W |
| GDMA_OUT_INT_CLR_CHO_REG | Interrupt clear bits of TX channel O | 0x0074 | WT |
| GDMA_IN_INT_RAW_CH1_REG | Raw status interrupt RX channel 1 | 0x00C8 | R/WTC/SS |
| GDMA_IN_INT_ST_CH1_REG | Masked interrupt bits of RX channel 1 | 0x00CC | RO |
| GDMA_IN_INT_ENA_CH1_REG | Interrupt enable bits of RX channel 1 | 0x00D0 | R/W |
| GDMA_IN_INT_CLR_CH1_REG | Interrupt clear bits of RX channel 1 | 0x00D4 | WT |
| GDMA_OUT_INT_RAW_CH1_REG | Raw status interrupt TX channel 1 | 0x0128 | R/WTC/SS |
| GDMA_OUT_INT_ST_CH1_REG | Masked interrupt bits of TX channel 1 | 0x012C | RO |
| GDMA_IN_INT_RAW_CH1_REG | Raw status interrupt RX channel 1 | 0x0130 | R/W |
| GDMA_IN_INT_CLR_CH1_REG | Interrupt clear bits of TX channel 1 | 0x0134 | WT |
| GDMA_IN_INT_ST_CH2_REG | Masked interrupt bits of RX channel 2 | 0x018C | RO |
| GDMA_IN_INT_ENA_CH2_REG | Interrupt enable bits of RX channel 2 | 0x0190 | R/W |
| GDMA_IN_INT_CLR_CH2_REG | Interrupt clear bits of RX channel 2 | 0x0194 | WT |
| GDMA_OUT_INT_RAW_CH2_REG | Raw status interrupt TX channel 2 | 0x01E8 | R/WTC/SS |
| GDMA_OUT_INT_ST_CH2_REG | Masked interrupt bits of TX channel 2 | 0x01EC | RO |
| GDMA_IN_INT_RAW_CH3_REG | Raw status interrupt RX channel 3 | 0x0248 | R/WTC/SS |
| GDMA_IN_INT_ST_CH3_REG | Masked interrupt bits of TX channel 3 | 0x024C | RO |

---

*Espressif Systems*

*Page: 370*

*Document Title: ESP32-S3 TRM (Version 1.7)*

*Feedback Link: Submit Documentation Feedback*