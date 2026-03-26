

```markdown
Chapter 40  MIPI CSI GoBack

Register 40.12. CSI_HOST_INT_ST_PHY_FATAL_REG (0x00E0)

(reserved)
31 | 2 | 1 | 0
----------------------------------------------------------------------------------------------------
| | | Reset

CSI_HOST_ST_PHY_ERRSOTSYNCHS_n (n: 0-1) Represents whether the PHY_ERRSOTSYNCHS_n error occurs.

O: Do not occur
1: Occur
(RC)

Register 40.13. CSI_HOST_INT_MSK_PHY_FATAL_REG (0x00E4)

(reserved)
31 | 2 | 1 | 0
----------------------------------------------------------------------------------------------------
| | | Reset

CSI_HOST_MASK_PHY_ERRSOTSYNCHS_n (n: 0-1) Configures whether to mask CSI_HOST_ST_PHY_ERRSOTSYNCHS_n.

O: Mask the error interrupt
1: Enable the error interrupt
(R/W)
```