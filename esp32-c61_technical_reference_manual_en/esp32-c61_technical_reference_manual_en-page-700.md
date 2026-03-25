

```markdown
Register 16.41. CPU_APM_FUNC_CTRL_REG (0x00C4)

CPU_APM_MO_FUNC_EN Configures whether to enable permission management for CPU_APM_CTRL MO.
- 0: Disable
- 1: Enable
(R/W)

CPU_APM_M1_FUNC_EN Configures whether to enable permission management for CPU_APM_CTRL M1.
- 0: Disable
- 1: Enable
(R/W)

Register 16.42. CPU_APM_MO_STATUS_REG (0x00C8)

CPU_APM_MO_EXCEPTION_STATUS Represents exception status.
- bit0: 1 represents permission restrictions
- bit1: 1 represents address out of bounds
(RO)
```