

```markdown
- SPI_USR_CONF: set `SPI_USR_CONF` before `SPIUSR` is set, to enable this transfer.
- SPI_USR_CONF_NXT: if segment `i` is not the final transaction of this whole DMA-controlled transfer, its `SPI_USR_CONF_NXT` bit should be set to 1.
- SPI_CONF_BITLEN: GP-SPI2 CS setup time and hold time are programmable independently in each segment, see Section 43.6 for detailed configuration. The CS high time in each segment is about:

  `(SPI_CONF_BITLEN + 5) × T_AHB_CLK`

The CS high time in CONF state can be set from 62.5 ns~3.2768 ms when `f_AHB_CLK` is 80 MHz.
`(SPI_CONF_BITLEN + 5)` will overflow from (0x40000 - SPI_CONF_BITLEN - 5) if `SPI_CONF_BITLEN` is larger than 0x3FFFA.

## 43.5.10 GP-SPI Works as a Slave

GP-SPI can be used as a slave to communicate with an SPI master. As a slave, GP-SPI supports 1-bit SPI, 2-bit dual SPI, 4-bit quad SPI, and QPI modes, with specific communication formats. To enable this mode, set `SPI_SLAVE_MODE` in register `SPI_SLAVE_REG`.

The CS signal must be held low during the transfer, and its falling/rising edges indicate the start/end of a single or segmented transfer. Take CS low-level effective as an example, when GP-SPI is used as a slave, the CS invalid duration (high-level) between each SPI transfer should not be less than 8 `T_AHB_CLK` to ensure that each transfer can end normally.

### 43.5.10.1 Configurable Communication Formats

When GP-SPI works as a slave, SPI full-duplex and half-duplex communications are available. To select from the two communications, configure `SPI_DOUTDIN` in register `SPI_USER_REG`.

Full-duplex communication means that input data and output data are transmitted simultaneously throughout the entire transaction. All bits are treated as input or output data, which means no command, address or dummy states are expected. The interrupt `SPI_TRANS_DONE_INT` is triggered once the transaction ends.

In half-duplex communication, the format is CMD+ADDR+DUMMY+DATA (DIN or DOUT).

- “DIN” means that an SPI master reads data from GP-SPI.
- “DOUT” means that an SPI master writes data to GP-SPI.

The detailed properties of each state are as follows:

1. **CMD:**
   - Indicate the function of SPI slave.
   - One byte from master to slave.
   - Only the values in Table 43.5-16 and Table 43.5-17 are valid.
   - Can be sent in 1-bit SPI mode or 4-bit QPI mode.

2. **ADDR:**
   - The address for `Wr_BUF` and `Rd_BUF` commands in CPU-controlled transfer, or placeholder bits in other transfers and can be defined by application.
```