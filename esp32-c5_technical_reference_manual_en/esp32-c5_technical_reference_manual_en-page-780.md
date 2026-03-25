

```markdown
Register 18.49. LP_APMO_FUNC_CTRL_REG (0x00C4)

LP_APMO_MO_FUNC_EN Configures to enable permission management for LP_APMO_CTRL MO.
(R/W)
```

```markdown
Register 18.50. LP_APMO_MO_STATUS_REG (0x00C8)

LP_APMO_MO_EXCEPTION_STATUS Represents exception status.
bit0: 1 represents permission restrictions
bit1: 1 represents address out of bounds
(RO)
```

```markdown
Register 18.51. LP_APMO_MO_STATUS_CLR_REG (0x00CC)

LP_APMO_MO_EXCEPTION_STATUS_CLR Configures to clear exception status. (WT)
```