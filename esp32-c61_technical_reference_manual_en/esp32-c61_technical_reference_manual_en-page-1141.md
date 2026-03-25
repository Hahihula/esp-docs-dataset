

```markdown
|Bit|31|30|29|28|27|26|25|24|23|22|21|20|19|18|17|16|15|14|13|12|11|10|9|8|7|6|5|4|3|2|1|0|
|:----|:-----|:-----|:---------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|
|Name|0x0|reserved||SDIO_SLCO_RX_DSCR_ERR_INT_ENA||SDIO_SLCO_TX_DSCR_ERR_INT_ENA||SDIO_SLCO_RX_DONE_INT_ENA||SDIO_SLCO_TX_DONE_INT_ENA||reserved||SDIO_SLCO_RX_EOF_INT_ENA||SDIO_SLCO_TX_EOF_INT_ENA||reserved||SDIO_SLCO_TX_OVF_INT_ENA||SDIO_SLCO_RX_OVF_INT_ENA||reserved||SDIO_SLCO_TX_FRHOST_BIT0_INT_ENA||SDIO_SLCO_RX_FRHOST_BIT0_INT_ENA||reserved||SDIO_SLCO_TX_FRHOST_BIT1_INT_ENA||SDIO_SLCO_RX_FRHOST_BIT1_INT_ENA||reserved||SDIO_SLCO_TX_FRHOST_BIT2_INT_ENA||SDIO_SLCO_RX_FRHOST_BIT2_INT_ENA||reserved||SDIO_SLCO_TX_FRHOST_BIT3_INT_ENA||SDIO_SLCO_RX_FRHOST_BIT3_INT_ENA||reserved||SDIO_SLCO_TX_FRHOST_BIT4_INT_ENA||SDIO_SLCO_RX_FRHOST_BIT4_INT_ENA||reserved||SDIO_SLCO_TX_FRHOST_BIT5_INT_ENA||SDIO_SLCO_RX_FRHOST_BIT5_INT_ENA||reserved||SDIO_SLCO_TX_FRHOST_BIT6_INT_ENA||SDIO_SLCO_RX_FRHOST_BIT6_INT_ENA||reserved||SDIO_SLCO_TX_FRHOST_BIT7_INT_ENA||SDIO_SLCO_RX_FRHOST_BIT7_INT_ENA|
|Reset|0x0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|
```

SDIO_SLC_FRHOST_BITn_INT_ENA (n: 0-7) Write 1 to enable interrupt SLC_FRHOST_BITn_INT (n: 0-7). (R/W)

SDIO_SLCO_RX_START_INT_ENA Write 1 to enable interrupt SLCO_RX_START_INT. (R/W)

SDIO_SLCO_TX_START_INT_ENA Write 1 to enable interrupt SLCO_TX_START_INT. (R/W)

SDIO_SLCO_RX_UDF_INT_ENA Write 1 to enable interrupt SLCO_RX_UDF_INT. (R/W)

SDIO_SLCO_TX_OVF_INT_ENA Write 1 to enable interrupt SLCO_TX_OVF_INT. (R/W)

SDIO_SLCO_TX_DONE_INT_ENA Write 1 to enable interrupt SLCO_TX_DONE_INT. (R/W)

SDIO_SLCO_TX_SUC_EOF_INT_ENA Write 1 to enable interrupt SLCO_TX_SUC_EOF_INT. (R/W)

SDIO_SLCO_RX_DONE_INT_ENA Write 1 to enable interrupt SLCO_RX_DONE_INT. (R/W)

SDIO_SLCO_RX_EOF_INT_ENA Write 1 to enable interrupt SLCO_RX_EOF_INT. (R/W)

SDIO_SLCO_TX_DSCR_ERR_INT_ENA Write 1 to enable interrupt SLCO_TX_DSCR_ERR_INT. (R/W)

SDIO_SLCO_RX_DSCR_ERR_INT_ENA Write 1 to enable interrupt SLCO_RX_DSCR_ERR_INT. (R/W)
```