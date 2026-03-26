

```markdown
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| **Configuration registers**                |                                                                             |           |        |
| SDHOST_CTRL_REG                            | Control register                                                            | 0x0000    | R/W    |
| SDHOST_CLKDIV_REG                          | Clock divider configuration                                                 | 0x0008    | R/W    |
| SDHOST_CLKSRC_REG                          | Clock source selection                                                      | 0x000C    | R/W    |
| SDHOST_CLKENA_REG                          | Clock enable register                                                       | 0x0010    | R/W    |
| SDHOST_TMOOUT_REG                          | Data and response timeout configuration                                    | 0x0014    | R/W    |
| SDHOST_CTYPE_REG                           | Card bus width configuration                                                | 0x0018    | R/W    |
| SDHOST_BLKSIZE_REG                         | Card data block size configuration                                          | 0x001C    | R/W    |
| SDHOST_BYTCNT_REG                          | Data transfer length configuration                                         | 0x0020    | R/W    |
| SDHOST_CMDARG_REG                          | Command argument data                                                       | 0x0028    | R/W    |
| SDHOST_CMD_REG                             | Command and boot configuration                                              | 0x002C    | R/W    |
| SDHOST_FIFOTH_REG                          | FIFO configuration                                                          | 0x004C    | R/W    |
| SDHOST_DEBNCE_REG                          | Debounce filter time configuration                                         | 0x0064    | R/W    |
| SDHOST_USRID_REG                           | User ID (scratchpad)                                                        | 0x0068    | R/W    |
| SDHOST_VERID_REG                           | Version ID (scratchpad) register                                            | 0x006C    | RO     |
| SDHOST_HCON_REG                            | Hardware feature register                                                   | 0x0070    | RO     |
| SDHOST_UHS_REG                             | UHS-1                                                                       | 0x0074    | R/W    |
| SDHOST_RST_N_REG                           | Card reset                                                                  | 0x0078    | R/W    |
| SDHOST_BMOD_REG                            | Burst mode transfer configuration                                          | 0x0080    | R/W    |
| SDHOST_PLDMND_REG                          | Poll demand configuration                                                   | 0x0084    | WO     |
| SDHOST_DBADDR_REG                          | Linked-list base address                                                     | 0x0088    | R/W    |
| SDHOST_CARDTHRCTL_REG                      | Card Threshold Control                                                       | 0x0100    | R/W    |
| SDHOST_EMMCDDR_REG                         | eMMC DDR register                                                           | 0x010C    | R/W    |
| SDHOST_ENSHIFT_REG                         | Enable Phase Shift                                                          | 0x0110    | R/W    |
| SDHOST_CLK_EDGE_SEL_REG                    | SDIO control register                                                       | 0x0800    | R/W    |
| SDHOST_DLL_CLK_CONF_REG                    | SDIO DLL clock control                                                      | 0x0808    | R/W    |
| **Interrupt registers**                    |                                                                             |           |        |
| SDHOST_INTMASK_REG                         | SDIO interrupt mask register                                                 | 0x0024    | R/W    |
| SDHOST_MINTSTS_REG                         | Masked interrupt status register                                             | 0x0040    | RO     |
| SDHOST_RINTSTS_REG                         | Raw interrupt register                                                       | 0x0044    | R/W1C   |
| SDHOST_IDSTS_REG                           | DMA interrupt register                                                      | 0x008C    | R/W1C   |
| SDHOST_IDINTEN_REG                         | DMA interrupt enable register                                                | 0x0090    | R/W    |
| **Status registers**                       |                                                                             |           |        |
| SDHOST_RESP0_REG                           | Response data                                                               | 0x0030    | RO     |
| SDHOST_RESP1_REG                           | Long response data                                                          | 0x0034    | RO     |
| SDHOST_RESP2_REG                           | Long response data                                                          | 0x0038    | RO     |
| SDHOST_RESP3_REG                           | Long response data                                                          | 0x003C    | RO     |
```