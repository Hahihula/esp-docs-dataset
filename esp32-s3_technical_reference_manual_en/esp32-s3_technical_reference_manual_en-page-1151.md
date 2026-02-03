**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Table Reference and Continuation Note:**
- Table 30.10-2 – Continued from the previous page

**Transfer Type - Communication Mode Controlled by Interrupt**

1. If GDMA_IN_SUC_EOF_CHn_INT is triggered, it means all the RX data has been stored in the RX buffer.
   - The TX data has been sent to the slave.

2. SPITrans_DONE_INT is triggered when CS is high which indicates that master has completed the data exchange change in SPI_WO_REG ~ SPI_W15_REG with slave in this mode

3. SPI_SLV_WR_DMA_DONE_INT just means that the transmission on the SPI bus is done, but can not ensure that all the push data has been stored in the RX buffer.
   - For this reason, GDMA_IN_SUC_EOF_CHn_INT is recommended.

4. Or wait for SPI_SLV_WR_BUF_DONE_INT

5. Or wait for SPI_SLV_RD_DMA_DONE_INT

6. Or wait for SPI_SLV_RDBuf_DONE_INT

7. Slave should set the total read data byte length in SPI_MS_DATA_TITLEN before the transfer begins.
   - Set SPI_RX_EOF_EN to 1 before the end of the interrupt program.

8. Master and slave should define a method to end the segmented transfer, such as via GPIO interrupt
   - Master sends End_SEG_TRAN to end the segmented transfer or slave sets the total read data byte length in SPI_MS_DATA_BITLEN and waits for GDMA_IN_SUC_EOF_CHn_INT

9. Half-duplex WrBuf single transfer can be used in a slave segmented transfer.

10. Master sends End_SEG_TRAN to end the segmented transfer.
    - Half-duplex RdBuf single transfer can be used in a slave segmented transfer.

**Section Title:**
30.11 Register Summary

**Body Text:**
The addresses in this section are relative to SPI2/SPI3 base address provided in Table 4.3-3 in Chapter 4 System and Memory.
The abbreviations given in Column Access are explained in Section Access Types for Registers.

**Table of Registers with Columns Name, Description, SPI2 Address, SPI3 Address, Access**

| Name                   | Description                          | SPI2 Address   | SPI3 Address    | Access |
|------------------------|--------------------------------------|-----------------|------------------|-------|
| User-defined control registers |                             |                 |                  |       |
| SPI_CMD_REG           | Command control register             | 0x0000         | 0x0000          | varies |
| SPI_ADDR_REG          | Address value register               | 0x0004         | 0x0004          | R/W   |
| SPI_USER_REG          | SPI USER control register            | 0x0010         | 0x0010          | varies |
| SPI_USER1_REG         | SPI USER control register 1          | 0x0014         | 0x0014          | R/W   |
| SPI_USER2_REG         | SPI USER control register 2          | 0x0018         | 0x0018          | R/W   |
| Control and configuration registers |                    |                 |                  |       |
| SPI_CTRL_REG          | SPI control register                 | 0x0008         | 0x0008          | R/W   |
| SPI_MS_DLEN_REG       | SPI data bit length control register | 0x001C         | 0x001C          | R/W   |
| SPI_MISD_REG          | SPI misc register                    | 0x0020         | 0x0020          | R/W   |
| SPI_DMA_CONF_REG     | SPI DMA control register             | 0x0030         | 0x0030          | varies |
| SPI_SLAVE_REG         | SPI slave control register           | 0x00E0         | 0x00E0          | varies |
| SPI_SLAVE1_REG       | SPI slave control register 1         | 0x00E4         | 0x00E4          | R/W/SS|
| Clock control registers |                    |                 |                  |       |
| SPI_CLOCK_REG         | SPI clock control register           | 0x000C         | 0x000C          | R/W   |

**Footer:**
Espressif Systems
1151 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback