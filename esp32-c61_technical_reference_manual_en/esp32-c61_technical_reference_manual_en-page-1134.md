

```markdown
Register 30.20. SDIO_SLCO_LEN_CONF_REG (0x00F4)

| 31 | 23 | 22 | 21 | 20 | 19 |
|----|----|----|----|----|----|
|    |    |    |    |    |    |
| 0x20 | 0 | 0 |    | Oxo | Reset |

SDIO_SLCO_LEN_WDATA Configures the length of the data that the slave wants to send. (WT)

SDIO_SLCO_LEN_WR Configures this bit to 1 to write SDIO_SLCO_LEN_WDATA into SDIO_SLCO_LEN and SLCHOST_HOSTSLCHOST_SLCO_LEN. (WT)

SDIO_SLCO_LEN_INC Configures this bit to 1 to add 1 to SDIO_SLCO_LEN and SL- CHOST_HOSTSLCHOST_SLCO_LEN. (WT)

SDIO_SLCO_LEN_INC_MORE Configures this bit to 1 to add the value of SDIO_SLCO_LEN_WDATA to SDIO_SLCO_LEN and SLCHOST_HOSTSLCHOST_SLCO_LEN. (WT)


Register 30.21. SDIO_SLCO_TX_SHAREMEM_START_REG (0x0154)

| 31 |    |
|----|-----|
|    | Oxo | Reset |

SDIO_SDIO_SLCO_TX_SHAREMEM_START_ADDR Configures SLCO host to slave channel AHB start address boundary. (R/W)
```