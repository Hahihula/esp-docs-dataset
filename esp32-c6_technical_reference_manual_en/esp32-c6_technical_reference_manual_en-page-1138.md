
```markdown
Register 34.16. SDIO_SLCOTOKEN1_REG (0x0064)

| 31 | 28 | 27 | 16 | 15 | 14 | 13 | 12 | 11 | 0 |
|-----|----:|----:|----:|----:|----:|----:|----:|----:|---|
| Ox0 |     |     | Ox0 |   0 |   0 |   0 |   0 |    | Reset |

SDIO_SLCO_TOKEN1_WDATA Configures SLCO token 1 value. (WT)

SDIO_SLCO_TOKEN1_WR Configures this bit to 1 to write SDIO_SLCO_TOKEN1_WDATA into SDIO_SLCO_TOKEN1. (WT)

SDIO_SLCO_TOKEN1_INC Configures this bit to 1 to add 1 to SDIO_SLCO_TOKEN1. (WT)

SDIO_SLCO_TOKEN1_INC_MORE Configures this bit to 1 to add the value of SDIO_SLCO_TOKEN1_WDATA to SDIO_SLCO_TOKEN1. (WT)

SDIO_SLCO_TOKEN1 Represents the SLCO accumulated number of buffers for receiving packets. (RO)


Register 34.17. SDIO_SLC1TOKEN1_REG (0x006C)

| 31 | 28 | 27 | 16 | 15 | 14 | 13 | 12 | 11 | 0 |
|-----|----:|----:|----:|----:|----:|----:|----:|----:|---|
| Ox0 |     |     | Ox0 |   0 |   0 |   0 |   0 |    | Reset |

SDIO_SLC1_TOKEN1_WDATA Configures SLC1 token1 value. (WT)

SDIO_SLC1_TOKEN1_WR Configures this bit to 1 to write SDIO_SLC1_TOKEN1_WDATA into SDIO_SLC1_TOKEN1. (WT)

SDIO_SLC1_TOKEN1_INC Configures this bit to 1 to add 1 to SDIO_SLC1_TOKEN1. (WT)

SDIO_SLC1_TOKEN1_INC_MORE Configures this bit to 1 to add the value of SDIO_SLC1_TOKEN1_WDATA to SDIO_SLC1_TOKEN1. (WT)

SDIO_SLC1_TOKEN1 Represents SLC1 accumulated number of buffers for receiving packets. (RO)
```