

```markdown
## Register 20.47. HP_SYSTEM_HP_CORE_DBUS_TIMEOUT_REG (0x0128)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|---------------------------------------------|-----------------------------------------------------------------------------|
| 31-16     | (reserved)                                 |                                                                             |
| 1         | HP_SYSTEM_CORE_DBUS_TIMEOUT_THRES          | Configures HP CPU0/1 DBUS timeout threshold. (R/W)                          |
| 0         | HP_SYSTEM_CORE_DBUS_TIMEOUT_EN             | Configures whether or not to enable timeout protection on HP CPU0/1 DBUS. (R/W) |

## Register 20.48. HP_SYSTEM_HP_ICM_CPU_H2X_CFG_REG (0x0138)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|---------------------------------------------|-----------------------------------------------------------------------------|
| 31-29     | (reserved)                                 |                                                                             |
| 2         | HP_SYSTEM_CPU_ICM_H2X_POST_WR_EN           | Configures whether or not to enable Post Write mode in AHB2AXI bridge for improved write performance. (R/W) |
| 1         | HP_SYSTEM_CPU_ICM_H2X_CUT_THROUGH_EN       | Configures whether or not to enable CUT Through mode in AHB2AXI bridge for improved write performance. (R/W) |
| 0         | HP_SYSTEM_CPU_ICM_H2X_BRIDGE_BUSY          | Indicates when AHB2AXI bridge is busy. (RO)                                 |
```