

```markdown
Register 14.64. PMS_CORE_O_IRAMO_PMS_MONITOR_2_REG (0x00BC)

| Bit Range | Field Description                                                                                      |
|-----------|----------------------------------------------------------------------------------------------------------|
| 31        | (reserved)                                                                                                |
| 29-28     | o                                                                                                      |
| 5-4       | PMS_CORE_O_IRAMO_PMS_MONITOR_VIOLATE_STATUS_ADDR                                                       |
| 3         | PMS_CORE_O_IRAMO_PMS_MONITOR_VIOLATE_STATUS_WORLD                                                     |
| 2         | PMS_CORE_O_IRAMO_PMS_MONITOR_VIOLATE_STATUS_LOADSTORE                                                |
| 1         | PMS_CORE_O_IRAMO_PMS_MONITOR_VIOLATE_STATUS_WR                                                       |
| 0         | PMS_CORE_O_IRAMO_PMS_MONITOR_VIOLATE_STATUS_ADDR                                                      |

PMS_CORE_O_IRAMO_PMS_MONITOR_VIOLATE_INTR Stores the interrupt status of CPU's unauthorized IBUS access. (RO)

PMS_CORE_O_IRAMO_PMS_MONITOR_VIOLATE_STATUS_WR Indicates the access direction. 1: write, 0: read. Note that this field is only valid when PMS_CORE_O_IRAMO_PMS_MONITOR_VIOLATE_STATUS_LOADSTORE is 1. (RO)

PMS_CORE_O_IRAMO_PMS_MONITOR_VIOLATE_STATUS_LOADSTORE Indicates the instruction direction. 1: load/store, 0: instruction execution. (RO)

PMS_CORE_O_IRAMO_PMS_MONITOR_VIOLATE_STATUS_WORLD Stores the privileged mode the CPU was in when the illegal access happened. 0x01: privilegedenvironment, 0x10: unprivileged environment. (RO)

PMS_CORE_O_IRAMO_PMS_MONITOR_VIOLATE_STATUS_ADDR Stores the address that CPU's IBUS was trying to access unauthorized. Note that this is an offset to 0x40000000 and the unit is 4, which means the actual address should be 0x40000000 + PMS_CORE_O_IRAMO_PMS_MONITOR_VIOLATE_STATUS_ADDR * 4. (RO)
```