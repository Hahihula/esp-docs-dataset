Title: Table 8.3-1. PRO_CPU, APP_CPU Interrupt Configuration

### Left Column:
**Header:** Peripheral Interrupt Configuration Register  
**Subheader:** Status Register No.

| Bit | Status Register Name | No. |
|-----|-----------------------|----|
|     |                       |    |
| 0   | DPORT_PRO_MAC_INTR_MAP_REG | 0 |
| 1   | DPORT_PRO_MAC_NMI_MAP_REG | 1 |
| ... | ...                   | ... |
| 37  | DPORT_PRO_SDIO_HOST_INTP_MAP_REG | 46 |

### Middle Column:
**Header:** Peripheral Interrupt Source  
**Subheader:** APP_CPU

| No. | Name | Status Register Bit |
|-----|------|---------------------|
|     |      |                     |
| 0   | MAC_INTR | ... |
| 1   | MAC_NMI | ... |
| ... | ...    | ...                |
| 46  | SDIO_HOST_INTP | ... |

### Right Column:
**Header:** Peripheral Interrupt Configuration Register  
**Subheader:** Status Register No.

| Bit | Status Register Name | No. |
|-----|-----------------------|----|
|     |                       |    |
| 0   | DPORT_APP_MAC_INTR_MAP_REG | 0 |
| 1   | DPORT_APP_MAC_NMI_MAP_REG | 1 |
| ... | ...                   | ... |
| 46  | SDIO_HOST_INTP_MAP_REG | 29 |

### Footer:
- Page number: "176"
- Document version and feedback information is present but not transcribed due to its nature as a footer.

The image contains detailed tables with multiple columns, each listing bits of the configuration register along with their corresponding status registers. The structure indicates it's part of an engineering or technical document related to interrupt configurations for CPU peripherals in embedded systems design documentation (ESP32 TRM).