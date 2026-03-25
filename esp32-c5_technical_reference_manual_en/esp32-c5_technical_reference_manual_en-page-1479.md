

```markdown
Register 39.28. SDIO_SLC1_RX_SHAREMEM_END_REG (0x0170)

SDIO_SDIOSLC1RXSHAREMEMENDADDR Configures SLC1 slave to host channel AHB end address boundary. (R/W)


Register 39.29. SDIO_SLC_BURST_LEN_REG (0x017C)

SDIOSLCOTXDATALEN Configures SLCO host to slave channel AHB burst type.
0: Can use incr4
1: Can use incr8
(R/W)

SDIOSLCO_RXDATALLEN Configures SLCO slave to host channel AHB burst type.
0: Can use incr and incr4
1: Can use incr and incr8
(R/W)

SDIOSLC1TXDATALLEN Configures SLC1 host to slave channel AHB burst type.
0: Can use incr4
1: Can use incr8
(R/W)

SDIOSLC1RXDATALLEN Configures SLC1 slave to host channel AHB burst type.
0: Can use incr and incr4
1: Can use incr and incr8
(R/W)
```