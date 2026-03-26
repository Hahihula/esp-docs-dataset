

```markdown
Chapter 37 Pixel-Processing Accelerator (PPA)

Register 37.28. PPA_SRM_PARAM_ERR_ST_REG (0x0078)

Continued from the previous page...

PPA_YDST_LEN_TOO_LARGE_ERR_ST Represents whether the vertical size of the image block after scaling in the SRM is larger than 8191.
O: Within 8191
1: Larger than 8191
(RO)

PPA_X_RX_SCAL_EQUAL_O_ERR_ST Represents whether the horizontal direction scaling factor of the SRM input image block is O.
O: Not O
1: O
(RO)

PPA_RX_DSCR_HB_ERR_ST Represents whether the sum of the horizontal direction image block size HB configured in the SRM input list and the horizontal offset X exceeds the entire image’s horizontal size HA.
O: Not exceeded
1: Exceeded
(RO)

PPA_XDST_LEN_TOO_SMALL_ERR_ST Represents whether the horizontal size of the image block after scaling in the SRM is O.
O: Not O
1: O
(RO)

PPA_XDST_LEN_TOO_LARGE_ERR_ST Represents whether the horizontal size of the image block after scaling in the SRM is larger than 8191.
O: Within 8191
1: Larger than 8191
(RO)

PPA_X_YUV420_RX_SCALE_ERR_ST Represents whether the parameters HA/HB/X of the SRM input list are odd when the input format is YUV420.
O: Even
1: Odd
(RO)

PPA_Y_YUV420_RX_SCALE_ERR_ST Represents whether the parameters VA/VB/Y of the SRM input list are odd when the input format is YUV420.
O: Even
1: Odd
(RO)

Continued on the next page...
```