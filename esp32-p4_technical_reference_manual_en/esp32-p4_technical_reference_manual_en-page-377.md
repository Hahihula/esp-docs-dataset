

```markdown
Register 5.12. DMAC_CHn_CTL1_REG (n: 1-4) (0x0100*n + 0x001C)

DMAC_CHn_ARLEN_EN    Configures whether to enable the length of the source burst transfer.
O: VDMA uses any possible value that is less than or equal to 16 as the length of the source burst transfer.
1: VDMA uses the value of DMAC_CHn_ARLEN as the length of the source burst transfer till the extent possible. The remaining transfers use the maximum possible burst transfer length. For example, if the data size is 192 bytes and the source burst transfer length DMAC_CHn_ARLEN is set to 128 bytes, then after transmitting 128 bytes, the remaining 64 bytes is the maximum possible burst transfer length.
(R/W)

DMAC_CHn_ARLEN    Configures the length of the source burst transfer. The specified burst length is used for source data transfer till the extent possible. The remaining transfers use the maximum possible value that is less than or equal to 16.
(R/W)

DMAC_CHn_AWLEN_EN    Configures whether to enable the length of the destination burst transfer.
O: VDMA uses any possible value that is less than or equal to 16 as the length of the destination burst transfer.
1: VDMA uses the value of DMAC_CHn_AWLEN as the length of the destination burst transfer till the extent possible. The remaining transfers use the maximum possible burst transfer length.
(R/W)

DMAC_CHn_AWLEN    Configures the length of the destination burst transfer. The specified burst length is used for destination data transfer till the extent possible. The remaining transfers use the maximum possible value that is less than or equal to 16.
(R/W)

DMAC_CHn_SRC_STAT_EN    Configures whether to enable fetch of source status.
This logic enables the fetch of the status from the source peripheral of channel n pointed to by DMAC_CHn_SSTATARO. The value is subsequently stored in DMAC_CHn_SSTAT. At the end of each block transfer, the status value is written back to the DMAC_CHn_SSTAT register of the linked list, if either source or destination peripheral uses linked-list-based multi-block transfer.
O: Do not fetch source status
1: Fetch source status and store the value in DMAC_CHn_SSTAT
(R/W)

Continued on the next page...
```