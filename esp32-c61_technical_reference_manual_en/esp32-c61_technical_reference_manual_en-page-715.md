

```markdown
Register 17.7. HP_SYSTEM_HP_PERI_TIMEOUT_ADDR_REG (0x001C)

HP_SYSTEM_HP_PERI_TIMEOUT_ADDR   Represents the address information of abnormal access.
(RO)
```

```markdown
Register 17.8. HP_SYSTEM_HP_PERI_TIMEOUT_UID_REG (0x0020)

HP_SYSTEM_HP_PERI_TIMEOUT_UID   Represents the master ID[4:0] and master permission[6:5]
when trigger timeout. For details, see Chapter 16 Permission Control (PMS). This register will be
cleared after the interrupt is cleared. (WTC)
```