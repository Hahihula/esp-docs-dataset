

```markdown
Register 34.28. SDIO_SLC1_RX_SHAREMEM_END_REG (0x0170)

SDIO_SDIOSLC1RXSHAREMEMENDADDR Configures SLC1 slave to host channel AHB end address boundary. (R/W)


Register 34.29. SDIO_SLC_BURST_LEN_REG (0x017C)

SDIOSLCO_TXDATA_BURST_LEN Configures SLCO host to slave channel AHB burst type.
0: Can use incr4
1: Can use incr8
(R/W)

SDIOSLCO_RXDATA_BURST_LEN Configures SLCO slave to host channel AHB burst type.
0: Can use incr and incr4
1: Can use incr and incr8
(R/W)

SDIOSLC1_TXDATA_BURST_LEN Configures SLC1 host to slave channel AHB burst type.
0: Can use incr4
1: Can use incr8
(R/W)

SDIOSLC1_RXDATA_BURST_LEN Configures SLC1 slave to host channel AHB burst type.
0: Can use incr and incr4
1: Can use incr and incr8
(R/W)
```