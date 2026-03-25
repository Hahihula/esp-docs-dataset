

```markdown
## Register 30.28. SDIO_SLC1_RX_SHAREMEM_END_REG (0x0170)

SDIO_SDIOSLC1RXSHAREMEMENDADDR Configures SLC1 slave to host channel AHB end address boundary. (R/W)


## Register 30.29. SDIO_SLC_BURST_LEN_REG (0x017C)

SDIO_SLCO_TXDATA_BURST_LEN Configures SLCO host to slave channel AHB burst type.
- 0: Can use incr4
- 1: Can use incr8
(R/W)

SDIO_SLCO_RXDATA_BURST_LEN Configures SLCO slave to host channel AHB burst type.
- 0: Can use incr and incr4
- 1: Can use incr and incr8
(R/W)

SDIO_SLC1_TXDATA_BURST_LEN Configures SLC1 host to slave channel AHB burst type.
- 0: Can use incr4
- 1: Can use incr8
(R/W)

SDIO_SLC1_RXDATA_BURST_LEN Configures SLC1 slave to host channel AHB burst type.
- 0: Can use incr and incr4
- 1: Can use incr and incr8
(R/W)
```