

```markdown
Register 40.20. CSI_HOST_INT_FORCE_PHY_REG (0x0118)

| Bit | Field Name                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | CS1_HOST_FORCE_PHY_ERRSOTH_1                                                |
| 29  | CS1_HOST_FORCE_PHY_ERRSOTH_0                                                |
| ... | ...                                                                         |
| 2   | (reserved)                                                                  |
| 1   | Reset                                                                       |
| 0   | Reset                                                                       |

CSI_HOST_FORCE_PHY_ERRSOTH_n (n: 0-1) Configures whether to force set CSI_HOST_ST_PHY_ERRSOTH_n to 1.
- 0: Do not force set
- 1: Force set
(R/W)

CSI_HOST_FORCE_PHY_ERRRESC_n (n: 0-1) Configures whether to force set CSI_HOST_ST_PHY_ERRRESC_n to 1.
- 0: Do not force set
- 1: Force set
(R/W)

Register 40.21. CSI_HOST_INT_ST_BNDRY_FRAME_FATAL_REG (0x0280)

| Bit | Field Name                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| ... | ...                                                                         |
| 5   | CS1_HOST_ST_ERR_F_BNDRY_MATCH_VC15                                        |
| 4   | CS1_HOST_ST_ERR_F_BNDRY_MATCH_VC14                                        |
| 3   | CS1_HOST_ST_ERR_F_BNDRY_MATCH_VC13                                        |
| 2   | CS1_HOST_ST_ERR_F_BNDRY_MATCH_VC12                                        |
| 1   | CS1_HOST_ST_ERR_F_BNDRY_MATCH_VC11                                        |
| 0   | Reset                                                                       |

CSI_HOST_ST_ERR_F_BNDRY_MATCH_VCn (n: 0-15) Represents whether the ERR_F_BNDRY_MATCH_VCn error occurs.
- 0: Do not occur
- 1: Occur
(RC)
```