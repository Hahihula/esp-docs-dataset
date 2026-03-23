
```markdown
Register 14.61. PMS_CORE_O_PIF_PMS_MONITOR_4_REG (0x0140)
```

| Bit Field | Description |
|-----------|-------------|
| 31        | (reserved) |
| 29-28     | Reserved    |
| 27        | Reset       |
| 26-25     | Reserved    |
| 24-23     | Reserved    |
| 22-21     | Reserved    |
| 20-19     | Reserved    |
| 18-17     | Reserved    |
| 16-15     | Reserved    |
| 14         | PMS_CORE_O_PIF_PMS_MONITOR_NONWORD_VIOLATE_EN |
| 13         | PMS_CORE_O_PIF_PMS_MONITOR_NONWORD_VIOLATE_CLR |

PMS_CORE_O_PIF_PMS_MONITOR_NONWORD_VIOLATE_CLR Set this bit to clear the interrupt triggered when CPU’s PIF bus tries to access RTC memory or peripherals using unsupported data type. (R/WL)

PMS_CORE_O_PIF_PMS_MONITOR_NONWORD_VIOLATE_EN Set this bit to enable interrupt when CPU’s PIF bus tries to access RTC memory or peripherals using unsupported data type. (R/WL)
```