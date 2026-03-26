

```markdown
Register 37.28. PPA_SRM_PARAM_ERR_ST_REG (0x0078)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | Reserved                                                                    |
| 30  | PPA_Y_UV420_TX_SCALE_ERR_ST                                                |
| 29  | PPA_X_UV420_RX_SCALE_ERR_ST                                                |
| 28  | PPA_X_UV420_RX_DST_LEN_TOO_LARGE_ERR_ST                                   |
| 27  | PPA_X_RX_SCALE_EQUAL_O_ERR_ST                                              |
| 26  | PPA_Y_RX_SCALE_EQUAL_O_ERR_ST                                              |
| 25  | PPA_TX_DSCR_VB_ERR_ST                                                      |
| 24  | PPA_TX_DSCR_HB_ERR_ST                                                      |
| 23  | PPA_YDST_LEN_TOO_SMALL_ERR_ST                                             |
| 22  | PPA_RX_DSCR_VB_ERR_ST                                                      |
| 15-0| Reset                                                                      |

PPA_TX_DSCR_VB_ERR_ST Represents whether the vertical size of the SRM output image block plus the vertical offset Y configured in the output list exceeds the vertical size of the entire image configured in the output list, VA.
O: Not exceeded
1: Exceeded
(RO)

PPA_TX_DSCR_HB_ERR_ST Represents whether the horizontal size of the SRM output image block plus the vertical offset X configured in the output list exceeds the horizontal size of the entire image configured in the output list, HA.
O: Not exceeded
1: Exceeded
(RO)

PPA_Y_RX_SCALE_EQUAL_O_ERR_ST Represents whether the vertical direction scaling factor of the SRM input image block is O.
O: Not O
1: O
(RO)

PPA_RX_DSCR_VB_ERR_ST Represents whether the sum of the vertical direction image block size VB configured in the SRM input list and the vertical offset Y exceeds the entire image's vertical size VA.
O: Not exceeded
1: Exceeded
(RO)

PPA_YDST_LEN_TOO_SMALL_ERR_ST Represents whether the vertical size of the image block after scaling in the SRM is O.
O: Not O
1: O
(RO)
```