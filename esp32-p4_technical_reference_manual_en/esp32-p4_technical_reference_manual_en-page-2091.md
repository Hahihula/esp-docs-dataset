

```markdown
## Register 40.22: CSI_HOST_INT_MSK_BNDRY_FRAME_FATAL_REG (0x0284)

CSI_HOST_MASK_ERR_F_BNDRY_MATCH_VCn (n: 0-15) Configures whether to mask `CSI_HOST_ST_ERR_F_BNDRY_MATCH_VCn`.

- 0: Mask the error interrupt
- 1: Enable the error interrupt
(R/W)
```

```markdown
## Register 40.23: CSI_HOST_INT_FORCE_BNDRY_FRAME_FATAL_REG (0x0288)

CSI_HOST_FORCE_ERR_F_BNDRY_MATCH_VCn (n: 0-15) Configures whether to force set `CSI_HOST_ST_ERR_F_BNDRY_MATCH_VCn` to 1.

- 0: Do not force set
- 1: Force set
(R/W)
```