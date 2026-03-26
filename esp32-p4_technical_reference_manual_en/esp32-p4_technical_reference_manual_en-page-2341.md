

```markdown
Register 43.88. LP_SPI_SLAVE_REG (0x00E0)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | (reserved) | LP_SPI_SLAVE_MODE | LP_SPI_SOFT_RESET | LP_SPI_SLV_WRBUF_BITLEN_EN | LP_SPI_SLV_RDBUF_BITLEN_EN | LP_SPI_RSCK_DATA_OUT | LP_SPI_CLK_MODE_13 | LP_SPI_CLK_MODE | Reset |
```

LP_SPI_CLK_MODE Configures LP-SPI clock mode.
0: LP-SPI clock is off when CS becomes inactive.
1: LP-SPI clock is delayed one cycle after CS becomes inactive.
2: LP-SPI clock is delayed two cycles after CS becomes inactive.
3: LP-SPI clock is always on.
(R/W)

LP_SPI_CLK_MODE_13 Configures clock mode.
0: SPI clock mode 1 and mode 3. See Table 43.7-2.
1: SPI clock mode 0 and mode 2. See Table 43.7-2.
(R/W)

LP_SPI_RSCK_DATA_OUT Configures the edge of output data.
0: Output data at TSCK rising edge.
1: Output data at RSCK rising edge.
(R/W)

LP_SPI_SLV_RDBUF_BITLEN_EN Configures whether or not to use SPI_SLAVE_DATA_BITLEN to store the data bit length of Rd_BUF transfer.
0: Not use
1: Use
(R/W)

LP_SPI_SLV_WRBUF_BITLEN_EN Configures whether or not to use SPI_SLAVE_DATA_BITLEN to store the data bit length of Wr_BUF transfer.
0: Not use
1: Use
(R/W)

LP_SPI_SLAVE_MODE Configures SPI work mode.
0: Master
1: Slave
(R/W)

LP_SPI_SOFT_RESET Configures whether to reset the SPI clock line, CS line, and data line via software.
0: Not reset
1: Reset
(WT)
```