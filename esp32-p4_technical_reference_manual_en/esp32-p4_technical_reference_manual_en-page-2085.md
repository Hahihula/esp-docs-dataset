

```markdown
Register 40.14. CSI_HOST_INT_FORCE_PHY_FATAL_REG (0x00E8)

31                                 2          1          0
+-------------------------------------------------------------------------------------------------+
| 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 | Reset |
+-------------------------------------------------------------------------------------------------+

CSI_HOST_FORCE_PHY_ERRSOTSYNCHS_n (n: 0-1) Configures whether to force set CSI_HOST_ST_PHY_ERRSOTSYNCHS_n to 1.
0: Do not force set
1: Force set
(R/W)

Register 40.15. CSI_HOST_INT_ST_PKT_FATAL_REG (0x00F0)

31                                 2          1          0
+-------------------------------------------------------------------------------------------------+
| 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 | Reset |
+-------------------------------------------------------------------------------------------------+

CSI_HOST_ST_ERR_ECC_DOUBLE Represents whether the ERR_ECC_DOUBLE error occurs.
0: Do not occur
1: Occur
(RC)

CSI_HOST_ST_SHORTER_PAYLOAD Represents whether the SHORTER_PAYLOAD error occurs.
0: Do not occur
1: Occur
(RC)
```