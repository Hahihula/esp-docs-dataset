

```markdown
Chapter 20 System Registers (SYSREG)

Register 20.74. HP_SYSTEM_ICM_DLOCK_STATUS_REG (0x0008)
```

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                 |                                                                             |
| 12  | HP_SYSTEM_ICM_DLOCK_WR     | Indicates whether the deadlocked transaction is a write operation.           |
| 11  |                             | O: Not a write operation                                                   |
| 10  | HP_SYSTEM_ICM_DLOCK_ID     | Records the AXID of the transaction that is deadlocked. (RO)                 |
| 7   | HP_SYSTEM_ICM_DLOCK_SLV    | Records the slave with which the deadlock has occurred. (RO)                 |
| 6   |                             |                                                                             |
| 4   | HP_SYSTEM_ICM_DLOCK_MST    | Records the lowest numbered master involved in a deadlock. (RO)              |
| 3   |                             |                                                                             |
| 0   | Reset                      |                                                                             |

HP_SYSTEM_ICM_DLOCK_MST Records the lowest numbered master involved in a deadlock. (RO)

HP_SYSTEM_ICM_DLOCK_SLV Records the slave with which the deadlock has occurred. (RO)

HP_SYSTEM_ICM_DLOCK_ID Records the AXID of the transaction that is deadlocked. (RO)

HP_SYSTEM_ICM_DLOCK_WR Indicates whether the deadlocked transaction is a write operation.
O: Not a write operation
1: Write operation
(RO)

Register 20.75. HP_SYSTEM_ICM_SYS_ADDRHOLE_ADDR_REG (0x0038)
```

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  |                             | 0x000000                                                                     |
|     | HP_SYSTEM_ICM_SYS_ADDRHOLE_ADDR | Records the address when ICM_SYS_ADDRHOLE_INT occurs. When HP_SYSTEM_ICM_SYS_ADDRHOLE_SECURE is 0, it records the unauthorized access address. When HP_SYSTEM_ICM_SYS_ADDRHOLE_SECURE is 1, it records the illegal access address. (RO) |

Espressif Systems

Submit Documentation Feedback

ESP32-P4 TRM
PRELIMINARY
```