

```markdown
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| SDIO_SLC1_RX_SHAREMEM_END_REG             | SLC1 AHB RX end address range                                              | 0x0170    | R/W    |
| SDIO_SLC_BURST_LEN_REG                    | DMA AHB burst type configuration                                          | 0x017C    | R/W    |

**Interrupt registers**

| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| SDIO_SLCOINT_RAW_REG                      | SLCO to slave raw interrupt status                                         | 0x0004    | varies |
| SDIO_SLCOINT_ST_REG                       | SLCO to slave masked interrupt status                                     | 0x0008    | RO     |
| SDIO_SLCOINT_ENA_REG                      | SLCO to slave interrupt enable                                            | 0x000C    | R/W    |
| SDIO_SLCOINT_CLR_REG                      | SLCO to slave interrupt clear                                             | 0x0010    | WT     |
| SDIO_SLC1INT_RAW_REG                      | SLC1 to slave raw interrupt status                                        | 0x0014    | varies |
| SDIO_SLC1INT_CLR_REG                      | SLC1 to slave interrupt clear                                             | 0x0020    | WT     |
| SDIO_SLCINTVEC_TOHOST_REG                 | Slave to host interrupt vector set                                        | 0x005C    | WT     |
| SDIO_SLC1INT_ST1_REG                      | SLC1 to slave masked interrupt status                                    | 0x014C    | RO     |
| SDIO_SLC1INT_ENA1_REG                     | SLC1 to slave interrupt enable                                           | 0x0150    | R/W    |

**Status registers**

| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| SDIO_SLCO_LENGTH_REG                      | Length of transmitting packets                                            | 0x00F8    | RO     |

## 30.8.3 SLC Host Register Summary

| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| **Configuration registers**                |                                                                             |           |        |
| SLCHOST_CONF_REG                          | Edge configuration                                                         | 0x01FO    | R/W    |

**Interrupt registers**

| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| SLCHOST_SLCOHOST_INT_RAW_REG              | SLCO to host raw interrupt status                                         | 0x0050    | varies |
| SLCHOST_SLC1HOST_INT_RAW_REG              | SLC1 to host raw interrupt status                                         | 0x0054    | varies |
| SLCHOST_SLCOHOST_INT_ST_REG               | SLCO to host masked interrupt status                                     | 0x0058    | RO     |
| SLCHOST_SLC1HOST_INT_ST_REG               | SLC1 to host masked interrupt status                                     | 0x005C    | RO     |
| SLCHOST_CONF_W7_REG                       | Host to slave interrupt vector set                                        | 0x008C    | R/W    |
| SLCHOST_SLCOHOST_INT_CLR_REG              | SLCO to host interrupt clear                                              | 0x00D4    | WT     |
| SLCHOST_SLC1HOST_INT_CLR_REG              | SLC1 to host interrupt clear                                              | 0x00D8    | WT     |
| SLCHOST_SLCOHOST_FUNC1_INT_ENA_REG        | SLCO to host interrupt enable                                            | 0x00DC    | R/W    |
| SLCHOST_SLC1HOST_FUNC1_INT_ENA_REG        | SLC1 to host interrupt enable                                            | 0x00EO    | R/W    |

**Status registers**

| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| SLCHOST_SLCOHOST_TOKEN_RDATA_REG          | Accumulated number of SLCO receiving buffers                              | 0x0044    | RO     |
| SLCHOST_PKT_LEN_REG                       | Length of the transmitting packets                                        | 0x0060    | RO     |
| SLCHOST_SLC1HOST_TOKEN_RDATA_REG          | Accumulated number of SLC1 receiving buffers                             | 0x00C4    | RO     |

**Communication Registers**

| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| SLCHOST_CONF_Wn_REG(n: 0-2)               | Host and slave communication                                             | 0x006C+0x4*n | R/W    |
| SLCHOST_CONF_W3_REG                        | Host and slave communication                                             | 0x0078    | R/W    |
| SLCHOST_CONF_W4_REG                        | Host and slave communication                                             | 0x007C    | R/W    |
```