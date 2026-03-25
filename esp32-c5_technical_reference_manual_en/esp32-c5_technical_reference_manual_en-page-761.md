

```markdown
Chapter 18 Permission Control (PMS)

Register 18.5. HP_APM_FUNC_CTRL_REG (0x00C4)
```
![Diagram of Register 18.5 with bit fields and descriptions](image_description: A register diagram showing bits 31 to 0, labeled as reserved for most high bits except the last few which are defined by specific function enable bits for HP_APM_CTRL M0 through M4. The reset values shown in binary format at the bottom right of the field.)

```markdown
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
Register 18.6. HP_APM_MO_STATUS_REG (0x00C8)
```
![Diagram of Register 18.6 with bit fields and descriptions](image_description: A register diagram showing bits 31 to 0, labeled as reserved for most high bits except the last few which are defined by exception status flags for HP_APM_MO_EXCEPTION_STATUS. The reset value is shown in binary format at the bottom right of the field.)

```markdown
HP_APM_MO_EXCEPTION_STATUS Represents exception status.
bit0: 1 represents permission restrictions
bit1: 1 represents address out of bounds
(RO)
```

Espressif Systems

761

ESP32-C5 TRM (Version 1.0)

Submit Documentation Feedback
```