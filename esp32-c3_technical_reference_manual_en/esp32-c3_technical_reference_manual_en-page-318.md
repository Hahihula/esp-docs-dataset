

```markdown
| Bus     | Environment   | Configuration Registers^A                                                                                      | Access |
|---------|---------------|-----------------------------------------------------------------------------------------------------------------|--------|
| IBUS    | Privileged    | PMS_CORE_X_IRAMO_PMS_CONSTRAIN_2_REG [20:18]^B                                                                | X/W/R  |
|         | Unprivileged  | PMS_CORE_X_IRAMO_PMS_CONSTRAIN_1_REG [20:18]^B                                                                 | X/W/R  |
| DBUS    | Privileged    | PMS_CORE_X_DRAMO_PMS_CONSTRAIN_1_REG [25:24]^C                                                                 | W/R    |
|         | Unprivileged  | PMS_CORE_X_DRAMO_PMS_CONSTRAIN_1_REG [27:26]                                                                    | W/R    |

^A 1: with access; 0: without access
^B For example, configuring this field to Ob101 indicates CPU's IBUS is granted instruction execution and read accesses but not write access to ROM in the unprivileged environment.
^C For example, configuring this field to Ob01 indicates CPU's DBUS is granted read access but not write access to ROM in privileged environment.

## 14.4.2 SRAM

ESP32-C3’s SRAM can be accessed by CPU’s instruction bus (IBUS) and data bus (DBUS) when configured. The SRAM address ranges accessible for IBUS and DBUS respectively are listed in Table 14.4-3.

Table 14.4-3. SRAM Address

| SRAM         | Block | IBUS Address Starting Address Ending Address | DBUS Address Starting Address Ending Address |
|--------------|-------|-----------------------------------------------|-----------------------------------------------|
| Internal SRAM0 | -     | 0x4037_C000                                  | -                                             |
|              |       |                                               |                                               |
|              | Block0| 0x4038_0000                                 | 0x3FC8_0000                                   |
| Internal SRAM1 | Block1| 0x403A_0000                                 | 0x3FCA_0000                                   |
|              | Block2| 0x403C_0000                                 | 0x3FCC_0000                                   |

Here, we will first introduce how to configure the permission to Internal SRAM0 and then Internal SRAM1.

### 14.4.2.1 Internal SRAM0 Access Configuration

ESP32-C3’s Internal SRAM0 can be allocated to either CPU or ICACHE.

Users can configure PMS_INTERNAL_SRAM_USAGE_CPU_CACHE to allocate ESP32-C3’s Internal SRAM0 to either CPU or ICACHE:

*   1: CPU
*   0: ICACHE

When the Internal SRAM0 is allocated to CPU, ESP32-C3 uses the registers listed in Table 14.4-4 to configure the instruction execution (X), write (W) and read (R) accesses of CPU’s IBUS, in the privileged environment and the unprivileged environment:
```