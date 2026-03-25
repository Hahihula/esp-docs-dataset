

```markdown
## 26.5.10.1 Configurable Communication Formats

When GP-SPI2 works as slave, full-duplex and half-duplex communications are available. To select from the two communications, configure SPI_DOUTDIN in register SPI_USER_REG.

Full-duplex communication means that input data and output data are transmitted simultaneously throughout the entire transaction. All bits are treated as input or output data, which means no command, address or dummy states are expected. The interrupt SPI_TRANS_DONE_INT is triggered once the transaction ends.

In half-duplex communication, the format is CMD+ADDR+DUMMY+DATA (DIN or DOUT).

*   "DIN" means that an SPI master reads data from GP-SPI2.
*   "DOUT" means that an SPI master writes data to GP-SPI2.

The detailed properties of each state are as follows:

1.  CMD:
    *   Indicate the function of SPI slave.
    *   One byte from master to slave.
    *   Only the values in Table 26.5-13 and Table 26.5-14 are valid.
    *   Can be sent in 1-bit SPI mode or 4-bit QPI mode.

2.  ADDR:
    *   The address for Wr_BUF and Rd_BUF commands in CPU-controlled transfer, or placeholder bits in other transfers and can be defined by application.
    *   One byte from master to slave.
    *   Can be sent in 1-bit, 2-bit, or 4-bit modes according to the command.

3.  DUMMY:
    *   Its value is meaningless. SPI slave prepares data in this state.
    *   Bit mode of FSPI bus is also meaningless here.
    *   Last for eight SPI_CLK cycles.

4.  DIN or DOUT:
    *   Data length can be 0~64 bytes in CPU-controlled transfer and unlimited in DMA-controlled transfer.
    *   Can be sent in 1-bit, 2-bit or 4-bit modes according to the CMD value.

**Note:**
The states of ADDR and DUMMY can never be skipped in any half-duplex communications.

When a half-duplex transaction is complete, the transferred CMD and ADDR values are latched into SPI_SLV_LAST_COMMAND and SPI_SLV_LAST_ADDR, respectively. SPI_SLV_CMD_ERR_INT_RAW will be set if the transferred CMD value is not supported by GP-SPI2 as slave. SPI_SLV_CMD_ERR_INT_RAW can only be cleared by software.
```