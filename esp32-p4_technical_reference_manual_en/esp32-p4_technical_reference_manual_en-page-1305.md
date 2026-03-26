

```markdown
Register 20.77. HP_SYSTEM_ICM_CPU_ADDRHOLE_ADDR_REG (0x0040)
```

| 31 | 0 |
|-----|----|
|     |    |
| 0x000000 | Reset |

HP_SYSTEM_ICM_CPU_ADDRHOLE_ADDR Records the address when ICM_CPU_ADDRHOLE_INT occurs.

When HP_SYSTEM_ICM_CPU_ADDRHOLE_SECURE is 0, it records the unauthorized access address.

When HP_SYSTEM_ICM_CPU_ADDRHOLE_SECURE is 1, it records the illegal access address. (RO)
```