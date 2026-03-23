
```markdown
Table 14.6-6. Access Configuration of IBUS to Split Regions

| Split Regions | Configuration Register | Access Configuration                                                                 |
|---------------|------------------------|---------------------------------------------------------------------------------------|
|               |                        | Privileged^A                     | Unprivileged^A                   |
| IBUS Region0^C | -                      | -                                 | -                               |
| IBUS Region1   | EXTMEM_IBUS_PMS_TBL_ATTR_REG | [1:0]^B                         | [3:2]                           |
| IBUS Region2   | EXTMEM_IBUS_PMS_TBL_ATTR_REG | [5:4]                           | [7:6]                           |
| IBUS Region3^C | -                      | -                                 | -                               |

^A These bits are configured in order R/X.
^B For example, configuring this field to 2'b10 indicates CPU's IBUS is granted read access but no instruction execution access to IBUS region1 in the privileged environment.
^C IBUS is not allowed to access Region0 and Region3, thus cannot be configured. All attempts will be rejected.

Table 14.6-7. Access Configuration of DBUS to Split Regions

| Split Regions | Configuration Register | Access Configuration                                                                 |
|---------------|------------------------|---------------------------------------------------------------------------------------|
|               |                        | Privileged^A                     | Unprivileged^A                   |
| DBUS Region0^C | -                      | -                                 | -                               |
| DBUS Region1   | EXTMEM_DBUS_PMS_TBL_ATTR_REG | [0]^B                           | [1]                             |
| DBUS Region2   | EXTMEM_DBUS_PMS_TBL_ATTR_REG | [2]                             | [3]                             |
| DBUS Region3^C | -                      | -                                 | -                               |

^A Only the read access can be configured.
^B For example, configuring this field to 1'b1 indicates CPU's DBUS is granted read access to DBUS region1 in the privileged environment.
^C DBUS is not allowed to access Region0 and Region3, thus cannot be configured. All attempts will be rejected.

## 14.7 Unauthorized Access and Interrupts

Any attempt to access ESP32-C3's slave device without configured permission is considered an unauthorized access and will be handled as described below:

* This attempt will only be responded with default values, in particular,
    * All instruction execution or read attempts will be responded with 0 (for internal memory and peripheral) or 0xdeadbeaf (for external memory)
    * All write attempts will fail
* An interrupt will be triggered (when enabled). See details below.

Note that only the information of the first interrupt is logged. Therefore, it's advised to handle interrupt signals and clear interrupts in-time, so the information of the next interrupt can be logged correctly.
```