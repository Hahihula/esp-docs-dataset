

```markdown
Chapter 18 Permission Control (PMS)

Register 18.12. HP_APM_M1_EXCEPTION_INFO0_REG (0x00E0)

31       23      22     18   17    16    15        0
+--------+------+------+------+------+------+------+
| RESERVED | HP_APM_M1_EXCEPTION_ID | HP_APM_M1_EXCEPTION_MODE | HP_APM_M1_EXCEPTION_REGION |
+--------+------+------+------+------+------+------+

HP_APM_M1_EXCEPTION_REGION Represents the region where an exception occurs. (RO)
HP_APM_M1_EXCEPTION_MODE   Represents the master's security mode when an exception occurs. (RO)
HP_APM_M1_EXCEPTION_ID     Represents master ID when an exception occurs. (RO)

Register 18.13. HP_APM_M1_EXCEPTION_INFO1_REG (0x00E4)

31
+---------------------------------------------------------------+
| HP_APM_M1_EXCEPTION_ADDR                                    |
+---------------------------------------------------------------+

HP_APM_M1_EXCEPTION_ADDR Represents the access address when an exception occurs. (RO)
```