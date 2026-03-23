

# 38.9 Register Summary

The addresses in this section are relative to Parallel IO Controller base address provided in Table 5.3-2 in Chapter 5 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| **PARLIO RX Configuration Registers** | | | |
| `PARL_IO_RX_CFG0_REG` | PARLIO RX module configuration register 0 | 0x0000 | R/W |
| `PARL_IO_RX_CFG1_REG` | PARLIO RX module configuration register 1 | 0x0004 | varies |
| **PARLIO TX Configuration Registers** | | | |
| `PARL_IO_TX_CFG0_REG` | PARLIO TX module configuration register 0 | 0x0008 | R/W |
| `PARL_IO_TX_CFG1_REG` | PARLIO TX module configuration register 1 | 0x000C | R/W |
| **PARLIO TX Status Register** | | | |
| `PARL_IO_ST_REG` | PARLIO module status register 0 | 0x0010 | RO |
| **PARLIO Interrupt Configuration and Status Registers** | | | |
| `PARL_IO_INT_ENA_REG` | PARLIO interrupt enable register | 0x0014 | R/W |
| `PARL_IO_INT_RAW_REG` | PARLIO interrupt raw register | 0x0018 | R/SS/WTC |
| `PARL_IO_INT_ST_REG` | PARLIO interrupt status register | 0x001C | RO |
| `PARL_IO_INT_CLR_REG` | PARLIO interrupt clear register | 0x0020 | WT |
| **PARLIO Clock Gating Configuration Register** | | | |
| `PARL_IO_CLK_REG` | PARLIO clock configuration register | 0x0120 | R/W |
| **PARLIO Version Register** | | | |
| `PARL_IO_VERSION_REG` | Version control register | 0x03FC | R/W |