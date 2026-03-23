

```markdown
Register 28.10. SPI_SLAVE_REG (0x00E0)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  |    | 10 | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  |
|     |    | (reserved) | SPI_MST_FD_WAIT_DMA_TX_DATA | SPI_USR_CONF | SPI_SOFT_RESET | SPI_SLAVE_MODE | SPI_DMA_SEG_MAGIC_VALUE | (reserved) | SPI_SLV_WRDMABITLEN_EN | SPI_SLV_RDMA_BITLEN_EN | SPI_RSCCK_DATA_OUT | SPI_CLK_MODE_13 | SPI_CLK_MODE |
```

### SPI_CLK_MODE Configures SPI clock mode. (R/W)
- 0: SPI clock is off when CS becomes inactive.
- 1: SPI clock is delayed one cycle after CS becomes inactive.
- 2: SPI clock is delayed two cycles after CS becomes inactive.
- 3: SPI clock is always on.

Can be configured in CONF state.

### SPI_CLK_MODE_13 Configure clock mode. (R/W)
- 0: Support SPI clock mode 0 or 2. See Table 28.7-2.
- 1: Support SPI clock mode 1 or 3. See Table 28.7-2.

### SPI_RSCK_DATA_OUT Configures the edge of output data. (R/W)
- 0: Output data at TSCK rising edge.
- 1: Output data at RSCK rising edge.

### SPI_SLV_RDMA_BITLEN_EN Configures whether or not to use SPI_SLV_DATA_BITLEN to store the data bit length of Rd_DMA transfer. (R/W)
- 0: Not use
- 1: Use

### SPI_SLV_WRDMA_BITLEN_EN Configures whether or not to use SPI_SLV_DATA_BITLEN to store the data bit length of Wr_DMA transfer. (R/W)
- 0: Not use
- 1: Use

Continued on the next page...
```