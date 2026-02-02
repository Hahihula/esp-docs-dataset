**Chapter Title:**
Chapter 20 SPI Controller (SPI)

**Bullet Points:**
- SPI_IN_ERR_EOF_INT: Triggered when there is an error receiving linked lists.
- SPI_IN_DONE_INT: Triggered when the last received linked list had a length of 0.
- SPI_INLINK_DSCR_ERROR_INT: Triggered when the received linked list is invalid.
- SPI_OUTLINK_DSCR_ERROR_INT: Triggered when the linked list to be sent is invalid.
- SPI_INLINK_DSCR_EMPTY_INT: Triggered when no valid linked list is available.

**Section Title:**
20.7 Register Summary

**Body Text:**
The addresses in this section are relative to the SPI base address provided in Table 3.3-6 in Chapter 3 System and Memory.
The abbreviations given in Column Access are explained in Section Access Types for Registers.

**Table Headers:**
- Name
- Description
- SPI0
- SPI1
- SPI2
- SPI3
- Acc

**Table Content (Summary of Columns):**

| Control and configuration registers | |
|---|---|
| SPI_CTRL_REG | Bit order and QIO/DIO/QOUT/DOU mode settings | 3FF43008, 3FF42008, 3FF64008, 3FF65008 | R/W |
| SPI_CTRL2_REG | Timing configuration | 3FF43014, 3FF42014, 3FF64014, 3FF65014 | R/W |
| SPI_CLOCK_REG | Clock configuration | 3FF43018, 3FF42018, 3FF64018, 3FF65018 | R/W |
| SPI_PIN_REG | Polarity and CS configuration | 3FF43034, 3FF42034, 3FF64034, 3FF65034 | R/W |

**Table Content (Slave mode configuration registers):**

| Slave mode configuration registers | |
|---|---|
| SPI_SLAVE_REG | Slave mode configuration and interrupt status | 3FF43038, 3FF42038, 3FF64038, 3FF65038 | R/W |
| SPI_SLAVE1_REG | Slave data bit lengths | 3FF4303C, 3FF4203C, 3FF6403C, 3FF6503C | R/W |
| SPI_SLAVE2_REG | Dummy cycle length configuration | 3FF43040, 3FF42040, 3FF64040, 3FF65040 | R/W |

**Table Content (Slave mode registers):**

| Slave mode registers | |
|---|---|
| SPI_SLV_WR_STATUS_REG | Slave status/Part of lower master address | 3FF4303O, 3FF4203O, 3FF6403O, 3FF6503O | R/W |
| SPI_SLV_WRBUFF_DLEN_REG | Write-buffer operation length | 3FF43048, 3FF42048, 3FF64048, 3FF65048 | R/W |
| SPI_SLV_RDBUF_DLEN_REG | Read-buffer operation length | 3FF4304C, 3FF4204C, 3FF6404C, 3FF6504C | R/W |
| SPI_SLV_RD_BIT_REG | Read data operation length | 3FF43064, 3FF42064, 3FF64064, 3FF65064 | R/W |

**Table Content (User-defined command mode registers):**

| User-defined command mode registers | |
|---|---|
| SPI_CMD_REG | Start user-defined command | 3FF43000, 3FF42000, 3FF64000, 3FF65000 | R/W |
| SPI_ADDR_REG | Address data | 3FF43004, 3FF42004, 3FF64004, 3FF65004 | R/W |

**Footer:**
Espressif Systems
Page number: 363
Document version (Version 5.6)