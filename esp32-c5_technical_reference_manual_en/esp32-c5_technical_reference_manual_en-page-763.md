

```markdown
Chapter 18 Permission Control (PMS)

Register 18.10. HP_APM_M1_STATUS_REG (0x00D8)
```
![HP_APM_M1_EXCEPTION_STATUS bitfield diagram](image_description: A horizontal bitfield labeled "HP_APM_M1_EXCEPTION_STATUS" with bits from 31 down to 0, marked as reserved for most positions except bit 2 and below which are shown as part of the status register. Bit 0 is associated with permission restrictions (bit0), bit 1 represents address out of bounds (bit1). The register has a reset value indicated at the bottom right.)

```markdown
HP_APM_M1_EXCEPTION_STATUS Represents exception status.
bit0: 1 represents permission restrictions
bit1: 1 represents address out of bounds
(RO)
```
Register 18.11. HP_APM_M1_STATUS_CLR_REG (0x00DC)
```
![HP_APM_M1_EXCEPTION_STATUS_CLR bitfield diagram](image_description: A horizontal bitfield labeled "HP_APM_M1_EXCEPTION_STATUS_CLR" with bits from 31 down to 0, mostly marked as reserved except for the least significant positions. The register has a reset value indicated at the bottom right.)

```markdown
HP_APM_M1_EXCEPTION_STATUS_CLR Configures to clear exception status. (WT)
```
Espressif Systems
763
ESP32-C5 TRM (Version 1.0)

Submit Documentation Feedback
```