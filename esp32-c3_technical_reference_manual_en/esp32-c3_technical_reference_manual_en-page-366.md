
```markdown
Register 14.32. PMS_CORE_O_IRAMO_PMS_MONITOR_1_REG (0x00B8)
```

| Bit Field | Description |
|-----------|-------------|
| 31-2       | (reserved)  |
| 1         | PMS_CORE_O_IRAMO_PMS_MONITOR_VIOLATE_EN |
| 0         | PMS_CORE_O_IRAMO_PMS_MONITOR_VIOLATE_CLR |

PMS_CORE_O_IRAMO_PMS_MONITOR_VIOLATE_CLR Set this bit to clear the interrupt triggered when CPU0's IBUS tries to access SRAM or ROM unauthorized. (R/WL)

PMS_CORE_O_IRAMO_PMS_MONITOR_VIOLATE_EN Set this bit to enable interrupt when CPU0's IBUS tries to access SRAM or ROM unauthorized. (R/WL)
```