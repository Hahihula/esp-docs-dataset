

```markdown
Register 33.20. TWAI_HW_CFG_REG (0x0084)

TWAI_HW_STANDBY_EN Configures whether to enable the standby function for hardware.
O: No effect
1: Enable the standby function for hardware
(R/W | R/W)
```

```markdown
Register 33.21. TWAI_HW_STANDBY_CNT_REG (0x0070)

TWAI_STANDBY_WAIT_CNT Configures the time required before hardware triggers the standby signal after entering idle status. (R/W | R/W)
Measurement unit: TWAI controller clock cycles.
```

```markdown
Register 33.22. TWAI_IDLE_INTR_CNT_REG (0x0070)

TWAI_IDLE_INTR_CNT Configures the time required before hardware generates the bus idle status interrupt signal after entering idle status. (R/W | R/W)
Measurement unit: TWAI controller clock cycles.
```