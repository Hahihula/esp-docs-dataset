

```markdown
Chapter 19 Permission Control (PMS)	605back
Register 19.71. PMS_LP_MM_PMS_REGO_REG (0x0008)

Continued from the previous page...

PMS_LP_MM_CPU_BUS_MON_ALLOW Configures whether the LP CPU in machine mode has permission to access CPU bus monitor.
O: Not allowed
1: Allowed
(R/W)

PMS_LP_MM_L2MEM_MON_ALLOW Configures whether the LP CPU in machine mode has permission to access L2MEM monitor.
O: Not allowed
1: Allowed
(R/W)

PMS_LP_MM_SPM_MON_ALLOW Configures whether the LP CPU in machine mode has permission to access SPM monitor.
O: Not allowed
1: Allowed
(R/W)

PMS_LP_MM_CACHE_ALLOW Configures whether the LP CPU in machine mode has permission to access cache.
O: Not allowed
1: Allowed
(R/W)
```