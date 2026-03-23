

```markdown
Register 27.10. SPI_SLAVE_REG (0x00E0)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 10 | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | SPI_CLK_MODE | SPI_RSCCK_DATA_OUT | SPI_SLV_WRBUF_BITLEN_EN | SPI_SLV_RDMA_BITLEN_EN | SPI_SLV_WRDMA_BITLEN_EN | SPI_SLV_RDBUF_BITLEN_EN | SPI_DMA_SEG_MAGIC_VALUE | SPI_SLAVE_MODE | SPI_SOFT_RESET | SPI_USR_CONF |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |             (reserved)             |                     |                     |                     |                     |                     |                     |                     |                     |                     |
| Reset | 0  | 0  | 0  | 0  | 0  | 0  | 10 | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  |
```

### SPI_CLK_MODE
SPI clock mode control bits. Can be configured in CONF state. (R/W)

- `0`: SPI clock is off when CS becomes inactive.
- `1`: SPI clock is delayed one cycle after CS becomes inactive.
- `2`: SPI clock is delayed two cycles after CS becomes inactive.
- `3`: SPI clock is always on.

### SPI_CLK_MODE_13
Configure clock mode. (R/W)

- `1`: support SPI clock mode 1 and 3. Output data B[0]/B[7] at the first edge.
- `0`: support SPI clock mode 0 and 2. Output data B[1]/B[6] at the first edge.

### SPI_RSCCK_DATA_OUT
Save half a cycle when TSCK is the same as RSCK. 1: output data at RSCCK posedge. 0: output data at TSCK posedge. (R/W)

### SPI_SLV_RDMA_BITLEN_EN
If this bit is set, `SPI_SLV_DATA_BITLEN` is used to store the data bit length of Rd_DMA transfer. (R/W)

### SPI_SLV_WRDMA_BITLEN_EN
If this bit is set, `SPI_SLV_DATA_BITLEN` is used to store the data bit length of Wr_DMA transfer. (R/W)

### SPI_SLV_RDBUF_BITLEN_EN
If this bit is set, `SPI_SLV_DATA_BITLEN` is used to store data bit length of Rd_BUF transfer. (R/W)

### SPI_SLV_WRBUF_BITLEN_EN
If this bit is set, `SPI_SLV_DATA_BITLEN` is used to store data bit length of Wr_BUF transfer. (R/W)

### SPI_DMA_SEG_MAGIC_VALUE
Configure the magic value of BM table in DMA-controlled configurable segmented transfer. (R/W)

### SPI_SLAVE_MODE
Set SPI work mode. 1: slave mode. 0: master mode. (R/W)

### SPI_SOFT_RESET
Software reset enable bit. If this bit is set, the SPI clock line, CS line, and data line are reset. Can be configured in CONF state. (WT)

### SPI_USR_CONF
`1`: enable the CONF state of current DMA-controlled configurable segmented transfer, which means the configurable segmented transfer is started. `0`: This is not a configurable segmented transfer. (R/W)
```