

```markdown
## 30.8 Register Summary

The addresses in this section are relative to the SDIO Slave Controller base address provided in Table 4.3-2 in Chapter 4 System and Memory.

The abbreviations given in the Access column are explained in Section Access Types for Registers.

### 30.8.1 HINF Register Summary

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| **Configuration registers** | | | |
| HINF_CFG_DATA0_REG | SDIO CIS configuration | 0x0000 | R/W |
| HINF_CFG_DATA1_REG | SDIO configuration | 0x0004 | R/W |
| HINF_CFG_DATA7_REG | SDIO configuration | 0x001C | varies |
| HINF_CIS_CONF_Wn_REG(n: 0-7) | SDIO CIS configuration | 0x0020+0x4*n | R/W |
| HINF_CFG_DATA16_REG | SDIO CIS configuration | 0x0040 | R/W |
| **Status registers** | | | |
| HINF_CONF_STATUS_REG | SDIO CIS function 0 config0 status | 0x0054 | RO |

### 30.8.2 SLC Register Summary

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| **Configuration registers** | | | |
| SDIO_SLCCONFO_REG | DMA configuration | 0x0000 | R/W |
| SDIO_SLCORX_LINK_REG | SCLO RX linked list configuration | 0x003C | varies |
| SDIO_SLCORX_LINK_ADDR_REG | SCLO RX linked list address | 0x0040 | R/W |
| SDIO_SLCOTX_LINK_REG | SCLO TX linked list configuration | 0x0044 | varies |
| SDIO_SLCOTX_LINK_ADDR_REG | SCLO TX linked list address | 0x0048 | R/W |
| SDIO_SLC1RX_LINK_REG | SCL1 RX linked list configuration | 0x004C | varies |
| SDIO_SLC1RX_LINK_ADDR_REG | SCL1 RX linked list address | 0x0050 | R/W |
| SDIO_SLC1TX_LINK_REG | SCL1 TX linked list configuration | 0x0054 | varies |
| SDIO_SLC1TX_LINK_ADDR_REG | SCL1 TX linked list address | 0x0058 | R/W |
| SDIO_SLCOTOKEN1_REG | SLCO receiving buffer configuration | 0x0064 | varies |
| SDIO_SLC1TOKEN1_REG | SLC1 receiving buffer configuration | 0x006C | varies |
| SDIO_SLCCONF1_REG | DMA configuration | 0x0070 | R/W |
| SDIO_SLC_RX_DSCR_CONF_REG | DMA slave to host configuration register | 0x00A8 | R/W |
| SDIO_SLC0_LEN_CONF_REG | Length control of transmitting packets | 0x00F4 | varies |
| SDIO_SLC0_TX_SHAREMEM_START_REG | SLCO AHB TX start address range | 0x0154 | R/W |
| SDIO_SLC0_TX_SHAREMEM_END_REG | SLCO AHB TX end address range | 0x0158 | R/W |
| SDIO_SLC0_RX_SHAREMEM_START_REG | SLCO AHB RX start address range | 0x015C | R/W |
| SDIO_SLC0_RX_SHAREMEM_END_REG | SLCO AHB RX end address range | 0x0160 | R/W |
| SDIO_SLC1_TX_SHAREMEM_START_REG | SCL1 AHB TX start address range | 0x0164 | R/W |
| SDIO_SLC1_TX_SHAREMEM_END_REG | SCL1 AHB TX end address range | 0x0168 | R/W |
| SDIO_SLC1_RX_SHAREMEM_START_REG | SCL1 AHB RX start address range | 0x016C | R/W |
```