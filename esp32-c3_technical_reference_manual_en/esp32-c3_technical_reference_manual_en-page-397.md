

```markdown
Register 14.65. PMS_CORE_0_DRAMO_PMS_MONITOR_2_REG (0x00D0)
```

| Bit Field | Description |
|-----------|-------------|
| 31-28     | (reserved)  |
| 27        |             |
| 26        |             |
| 25        |             |
| 24        |             |
| 23        |             |
| 22        |             |
| 21        |             |
| 20        |             |
| 19        |             |
| 18        |             |
| 17        |             |
| 16        |             |
| 15        |             |
| 14        |             |
| 13        |             |
| 12        |             |
| 11        |             |
| 10        |             |
| 9         |             |
| 8         |             |
| 7         |             |
| 6         |             |
| 5         |             |
| 4         |             |
| 3         |             |
| 2         |             |
| 1         |             |
| 0         | Reset       |

PMS_CORE_0_DRAMO_PMS_MONITOR_VIOLATE_INTR Stores the interrupt status of dBUS unauthorized access. (RO)

PMS_CORE_0_DRAMO_PMS_MONITOR_VIOLATE_STATUS_WORLD Stores the privileged mode the CPU was in when the illegal access happened. 0x01: privilegedenvironment, 0x10: unprivileged environment. (RO)

PMS_CORE_0_DRAMO_PMS_MONITOR_VIOLATE_STATUS_ADDR Stores the address that CPU0’s dBUS was trying to access unauthorized. Note that this is an offset to 0x3c000000 and the unit is 16, which means the actual address should be 0x3c000000 + PMS_CORE_0_DRAMO_PMS_MONITOR_VIOLATE_STATUS_ADDR * 4. (RO)
```