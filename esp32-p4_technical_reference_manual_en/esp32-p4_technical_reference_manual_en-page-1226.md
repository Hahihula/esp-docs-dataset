

```markdown
Register 19.77: PMS_LP_MM_LP_PERI_PMS_REGO_REG (0x0008)

Continued from the previous page...

PMS_LP_MM_LP_TSENS_ALLOW Configures whether LP CPU in machine mode has permission to access LP temperature sensor.
O: Not allowed
1: Allowed
(R/W)

PMS_LP_MM_LP_HUK_ALLOW Configures whether LP CPU in machine mode has permission to access LP HUK (Hardware Unique Key).
O: Not allowed
1: Allowed
(R/W)

PMS_LP_MM_LP_TRNG_ALLOW Configures whether LP CPU in machine mode has permission to access LP TRNG.
O: Not allowed
1: Allowed
(R/W)

Register 19.78: PMS_PERI_REGIONn_LOW_REG (n: 0-1) (0x000C+0x8*n)
```

```markdown
31                                 2          1           0

+---------------------------------------------------------------+
|                                                               |
|               0x0000000                                Reset   |
|                                                               |
+---------------------------------------------------------------+

PMS_PERI_REGIONn_LOW Configures the high 30 bits of the start address of peripheral register's regionn. (R/W)
```