

```markdown
Chapter 18 Permission Control (PMS)

Register 18.66. CPU_APM_M1_STATUS_REG (0x00D8)
```

![CPU_APM_M1_EXCEPTION_STATUS register bitfield diagram](image_description: A horizontal bitfield labeled "reserved" spans most of the width, with bits 31 down to a certain position marked as reserved. Bit positions near the right end are labeled CPU_APM_M1_EXCEPTION_STATUS, showing bit values at reset (bit 2 and below being 0).)

```markdown
CPU_APM_M1_EXCEPTION_STATUS Represents exception status.
bit0: 1 represents permission restrictions
bit1: 1 represents address out of bounds
(RO)
```

Register 18.67. CPU_APM_M1_STATUS_CLR_REG (0x00DC)

![CPU_APM_M1_EXCEPTION_STATUS_CLR register bitfield diagram](image_description: A horizontal bitfield labeled "reserved" spans most of the width, with bits mostly reserved and a single writable bit at position near right end marked as CPU_APM_M1_EXCEPTION_STATUS_CLR. Reset value is 0.)

```markdown
CPU_APM_M1_EXCEPTION_STATUS_CLR Write 1 to clear exception status. (WT)
```

Espressif Systems

788

ESP32-C5 TRM (Version 1.0)

Submit Documentation Feedback
```