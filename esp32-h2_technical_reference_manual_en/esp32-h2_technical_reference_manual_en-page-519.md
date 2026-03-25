

```markdown
Chapter 15 Permission Control (PMS)

Register 15.12. HP_APM_M1_EXCEPTION_INFO0_REG (0x00E0)

31                 23 22 18 17 16 15           0
+------------------+-----+----+----+----+
|     (reserved)    |  O  |  O |  O | Reset |
+------------------+-----+----+----+----+

HP_APM_M1_EXCEPTION_REGION Represents the region where an exception occurs. (RO)
HP_APM_M1_EXCEPTION_MODE   Represents the master's security mode when an exception occurs. (RO)
HP_APM_M1_EXCEPTION_ID     Represents master ID when an exception occurs. (RO)

Register 15.13. HP_APM_M1_EXCEPTION_INFO1_REG (0x00E4)

31                 0
+------------------+-----+
|     (reserved)    | Reset |
+------------------+-----+

HP_APM_M1_EXCEPTION_ADDR Represents the access address when an exception occurs. (RO)
```