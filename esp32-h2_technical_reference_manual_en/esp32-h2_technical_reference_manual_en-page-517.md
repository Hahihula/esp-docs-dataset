

```markdown
Register 15.8. HP_APM_MO_EXCEPTION_INFO0_REG (0x00D0)

31                                 23 22                                     18 17   16    15
+-------------------------------------------------------------------------------------------------+
| 0 0 0 0 0 0 0 0 | O       | O         | Reset |
+-------------------------------------------------------------------------------------------------+

HP_APM_MO_EXCEPTION_REGION Represents the region where an exception occurs. (RO)
HP_APM_MO_EXCEPTION_MODE   Represents the master's security mode when an exception occurs. (RO)
HP_APM_MO_EXCEPTION_ID     Represents master ID when an exception occurs. (RO)

Register 15.9. HP_APM_MO_EXCEPTION_INFO1_REG (0x00D4)

31
+-------------------------------------------------------------------------------------------------+
| 0                                                                                               |
+-------------------------------------------------------------------------------------------------+

HP_APM_MO_EXCEPTION_ADDR Represents the access address when an exception occurs. (RO)
```