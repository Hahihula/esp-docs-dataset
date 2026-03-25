

```markdown
Chapter 18 Permission Control (PMS)

Register 18.63. CPU_APM_MO_STATUS_CLR_REG (0x00CC)
```

![CPU_APM_MO_EXCEPTION_STATUS_CLR register bitfield diagram](image_description: A horizontal bitfield labeled from bit 31 to bit 0, with bits 31-0 marked as "reserved" and the rightmost two bits showing a reset value of '0'. The label indicates this is for CPU_APM_MO_EXCEPTION_STATUS_CLR.)

```markdown
CPU_APM_MO_EXCEPTION_STATUS_CLR Write 1 to clear exception status. (WT)

Register 18.64. CPU_APM_MO_EXCEPTION_INFO0_REG (0x00D0)
```

![CPU_APM_MO_EXCEPTION_INFO0_REG register bitfield diagram](image_description: A horizontal bitfield labeled from bit 31 to bit 15, with bits 23-17 and 16-18 marked as reserved or specific fields. The rightmost two bits show a reset value of '0'. Fields include CPU_APM_MO_EXCEPTION_ID (bits 18:16), CPU_APM_MO_EXCEPTION_MODE (bit 15), and CPU_APM_MO_EXCEPTION_REGION (bits 23:22).)

```markdown
CPU_APM_MO_EXCEPTION_REGION Represents the region where an exception occurs. (RO)
CPU_APM_MO_EXCEPTION_MODE Represents the master's security mode when an exception occurs. (RO)
CPU_APM_MO_EXCEPTION_ID Represents master ID when an exception occurs. (RO)

Register 18.65. CPU_APM_MO_EXCEPTION_INFO1_REG (0x00D4)
```

![CPU_APM_MO_EXCEPTION_INFO1_REG register bitfield diagram](image_description: A horizontal bitfield labeled from bit 31 to the right, with bits showing a reset value of '0'. The label indicates this is for CPU_APM_MO_EXCEPTION_ADDR.)

```markdown
CPU_APM_MO_EXCEPTION_ADDR Represents the access address when an exception occurs. (RO)

Espressif Systems    787    ESP32-C5 TRM (Version 1.0)
Submit Documentation Feedback
```