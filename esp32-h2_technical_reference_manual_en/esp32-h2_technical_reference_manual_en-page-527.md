

```markdown
Register 15.29. LP_APM_FUNC_CTRL_REG (0x00C4)

LP_APM_MO_FUNC_EN Configures to enable permission management for LP_APM_CTRL MO.
(R/W)
```

```markdown
Register 15.30. LP_APM_MO_STATUS_REG (0x00C8)

LP_APM_MO_EXCEPTION_STATUS Represents exception status.
bit0: 1 represents permission restrictions
bit1: 1 represents address out of bounds
(RO)
```

```markdown
Register 15.31. LP_APM_MO_STATUS_CLR_REG (0x00CC)

LP_APM_MO_REGION_STATUS_CLR Configures to clear exception status. (WT)
```