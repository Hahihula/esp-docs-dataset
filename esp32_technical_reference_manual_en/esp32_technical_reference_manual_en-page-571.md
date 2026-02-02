**Chapter Title:**
Chapter 26 SDIO Slave Controller (SDIO)

**List of Interrupts and Their Descriptions:**
- SLCOINT_SLCO_RX_EOF_INT - Slave sending operation is finished.
- SLCOINT_SLCO_RX_DONE_INT - A single buffer is sent by Slave.
- SLCOINT_SLCO_TXSuc_EOF_INT - Slave receiving operation is finished.
- SLCOINT_SLCO_TXDone_INT - A single buffer is finished during receiving operation.
- SLCOINT_SLCO_TXOVF_INT - Slave receiving buffer overflow interrupt.
- SLCOINT_SLCO_RX_UDF_INT - Slave sending buffer underflow interrupt.
- SLCOINT_SLCO_TX_START_INT - Slave receiving interrupt initialization.
- SLCOINT_SLCO_RX_START_INT - Slave sending interrupt initialization.
- SLCOINT_SLC_FRHOST_BITn_INT (n: 0 ~ 7) Host interrupts Slave.

**Section Title:**
26.4 Register Summary

**Body Text:**
The addresses in this section are relative to the SDIO Slave base address provided in Table 3.3-6 in Chapter 3 System and Memory.
The abbreviations given in Column Access are explained in Section Access Types for Registers.

**Table of SDIO DMA (SLC) configuration registers with columns Name, Description, Address, and Access:**
| Name                | Description                                    | Address       | Access |
|---------------------|-------------------------------------------------|---------------|--------|
| SLCCONFO_REG       | SLCCONFO_SLC configuration                      | 0x3FF58000   | R/W    |
| SLCORX_LINK_REG    | Transmitting linked list configuration           | 0x3FF5803C   | R/W    |
| SLCOTX_LINK_REG    | Receiving linked list configuration              | 0x3FF58040   | R/W    |
| SLCNTVEC_TOHOST_REG| Interrupt sector for Slave to interrupt Host     | 0x3FF5804C   | WO     |
| SLCOTOKEN1_REG     | Number of receiving buffer                       | 0x3FF58054   | WO     |
| SLCONF1_REG        | Control register                                | 0x3FF58060   | R/W    |
| SLC_RX_DSCR_CONF_REG| DMA transmission configuration                   | 0x3FF58098   | R/W    |
| SLCO_LEN_CONF_REG  | Length control of the transmitting packets       | 0x3FF580E4   | R/W    |
| SLCO_LENGTH_REG    | Length of the transmitting packets               | 0x3FF580E8   | R/W    |

**Table of Interrupt Registers with columns Name, Description, Address, and Access:**
| Name                | Description                                    | Address       | Access |
|---------------------|-------------------------------------------------|---------------|--------|
| SLCOINT_RAW_REG    | Raw interrupt status                            | 0x3FF58004   | RO     |
| SLCOINT_ST_REG     | Interrupt status                                | 0x3FF58008   | RO     |
| SLCOINT_ENA_REG    | Interrupt enable                                | 0x3FF580C    | R/W    |
| SLCOINT_CLR_REG    | Interrupt clear                                 | 0x3FF5810    | WO     |

**Table of SDIO SLC Host registers with columns Name, Description, Address, and Access:**
| Name                | Description                                    | Address       | Access |
|---------------------|-------------------------------------------------|---------------|--------|
| SLCOHOST_TOKEN_RDATA| The accumulated number of Slave's receiving buffers | 0x3FF55044   | RO     |
| SLCHOST_PKT_LEN_REG| Length of the transmitting packets              | 0x3FF55060   | R/W    |
| SLCHOST_CONF_WO_REG| Host and Slave communication register0          | 0x3FF5506C   | R/W    |
| SLCHOST_CONF_W1_REG| Host and Slave communication register1           | 0x3FF55070   | R/W    |
| SLCHOST_CONF_W2_REG| Host and Slave communication register2           | 0x3FF55074   | R/W    |

**Footer:**
Espressif Systems
Page number: 571
Document version (Version 5.6)
Submit Documentation Feedback