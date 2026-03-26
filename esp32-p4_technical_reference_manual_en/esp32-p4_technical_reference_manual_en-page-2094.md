

```markdown
Register 40.28. CSI_HOST_INT_MSK_CRC_FRAME_FATAL_REG (0x02A4)

31                                 16 15 14 13 12 11 10 9 8 7 6 5 4 3 2 1 0
+-------------------------------------------------------------------------------------------------+
| 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Reset |
+-------------------------------------------------------------------------------------------------+

CSI_HOST_MASK_ERR_FRAME_DATA_VCn (n: 0-15) Configures whether to mask CSI_HOST_ST_ERR_FRAME_DATA_VCn.
0: Mask the error interrupt
1: Enable the error interrupt
(R/W)

Register 40.29. CSI_HOST_INT_FORCE_CRC_FRAME_FATAL_REG (0x02A8)

31                                 16 15 14 13 12 11 10 9 8 7 6 5 4 3 2 1 0
+-------------------------------------------------------------------------------------------------+
| 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Reset |
+-------------------------------------------------------------------------------------------------+

CSI_HOST_FORCE_ERR_FRAME_DATA_VCn (n: 0-15) Configures whether to force set CSI_HOST_ST_ERR_FRAME_DATA_VCn to 1.
0: Do not force set
1: Force set
(R/W)
```