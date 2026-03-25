

```markdown
Register 16.5. HP_APM_FUNC_CTRL_REG (0x00C4)

HP_APM_MO_FUNC_EN Configures to enable permission management for HP_APM_CTRL MO.
(R/W)

HP_APM_M1_FUNC_EN Configures to enable permission management for HP_APM_CTRL M1.
(R/W)

HP_APM_M2_FUNC_EN Configures to enable permission management for HP_APM_CTRL M2.
(R/W)

HP_APM_M3_FUNC_EN Configures to enable permission management for HP_APM_CTRL M3.
(R/W)

HP_APM_M4_FUNC_EN Configures to enable permission management for HP_APM_CTRL M4.
(R/W)
```

```markdown
Register 16.6. HP_APM_MO_STATUS_REG (0x00C8)

HP_APM_MO_EXCEPTION_STATUS Represents exception status.

bit0: 1 represents permission restrictions

bit1: 1 represents address out of bounds

(RO)
```