

```markdown
Register 14.84.EXTMEM_DBUS_PMS_TBL_LOCK_REG (0x00EC)
```

| 31 | ... | 1 | 0 |
|----:|-----|---:|:-|
|    |     | Reset | EXTMEM_DBUS_PMS_LOCK |

EXTMEM_DBUS_PMS_LOCK Set this bit to lock DBUS' access to Cache DBUS regions. (R/W)

Register 14.85.EXTMEM_DBUS_PMS_TBL_BOUNDARYO_REG (0x00FO)
```

| 31 | ... | 12 | 11 | ... | 0 |
|----:|-----|----:|----:|-----|:-|
|    |     |     |     | Reset | EXTMEM_DBUS_PMS_BOUNDARYO |

EXTMEM_DBUS_PMS_BOUNDARYO Configures the starting address of Cache DBUS Region1. (R/W)
```