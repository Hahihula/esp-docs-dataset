

```markdown
Register 40.19. CSI_HOST_INT_MSK_PHY_REG (0x0114)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                             |                                                                             |
| 30-2 | reserved                                   |                                                                             |
| 18  | CSI_HOST_MASK_PHY_ERRSOTH_1                | Configures whether to mask CSI_HOST_ST_PHY_ERRSOTH_1                        |
| 17  |                                             |                                                                             |
| 16  | CSI_HOST_MASK_PHY_ERRSOTH_0                | Configures whether to mask CSI_HOST_ST_PHY_ERRSOTH_0                        |
| 15  |                                             |                                                                             |
| 14-2 | reserved                                   |                                                                             |
| 1   | Reset                                      |                                                                             |
| 0   |                                             |                                                                             |

CSI_HOST_MASK_PHY_ERRSOTH_n (n: 0-1) Configures whether to mask CSI_HOST_ST_PHY_ERRSOTH_n.
0: Mask the error interrupt
1: Enable the error interrupt
(R/W)

CSI_HOST_MASK_PHY_ERRESC_n (n: 0-1) Configures whether to mask CSI_HOST_ST_PHY_ERRESC_n.
0: Mask the error interrupt
1: Enable the error interrupt
(R/W)
```