

```markdown
Register 14.88.EXTMEM_DBUS_PMS_TBL_ATTR_REG (0x00FC)

| Bit | Description |
|-----|-------------|
| 31  | (reserved)  |
| 3   | EXTMEM_DBUS_PMS_SCT2_ATTR |
| 2   | EXTMEM_DBUS_PMS_SCT1_ATTR |
| 1   | Reset       |
| 0   | PM5         |

EXTMEM_DBUS_PMS_SCT1_ATTR Configures DBUS' access to Cache DBUS Region1.
Bit 0: Read access in the privileged environment
Bit 1: Read access in the unprivileged environment
(R/W)

EXTMEM_DBUS_PMS_SCT2_ATTR Configures DBUS' access to Cache DBUS Region2.
Bit 0: Read access in the privileged environment
Bit 1: Read access in the unprivileged environment
(R/W)
```