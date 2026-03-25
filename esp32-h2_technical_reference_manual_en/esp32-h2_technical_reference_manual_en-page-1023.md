

```markdown
Register 34.20. TWAI_HW_CFG_REG (0x0084)
```

```markdown
TWAI_HW_STANDBY_EN Configures whether to enable the standby function for hardware.

O: No effect
1: Enable the standby function for hardware
(R/W | R/W)
```

```markdown
Register 34.21. TWAI_HW_STANDBY_CNT_REG (0x0070)
```

```markdown
TWAI_STANDBY_WAIT_CNT Configures the time required before hardware triggers the standby signal after entering idle status. (R/W | R/W)

Measurement unit: TWAI controller clock cycles.
```

```markdown
Register 34.22. TWAI_IDLE_INTR_CNT_REG (0x0070)
```

```markdown
TWAI_IDLE_INTR_CNT Configures the time required before hardware generates the bus idle status interrupt signal after entering idle status. (R/W | R/W)

Measurement unit: TWAI controller clock cycles.
```
```markdown
Espressif Systems
1023
ESP32-H2 TRM (Version 1.1)
Submit Documentation Feedback
```