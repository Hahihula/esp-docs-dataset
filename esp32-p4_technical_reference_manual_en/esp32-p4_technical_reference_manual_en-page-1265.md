

# Chapter 20 System Registers (SYSREG)

## Register 20.16. HP_SYSTEM_CACHE_RESET_CONFIG_REG (0x0024)

```
31
+---------------------------------------------------------------+
| 6   5   4   3   2   1   0 |
| HP_SYSTEM_L1_I0_CACHE_RESET | HP_SYSTEM_L1_I1_CACHE_RESET | Reset |
| (reserved)                 | (reserved)                  |        |
+---------------------------------------------------------------+
```

**HP_SYSTEM_L1_D_CACHE_RESET** Configures whether or not to reset L1 dcache.  
- 0: No effect  
- 1: Reset  
(R/W)

**HP_SYSTEM_L1_I1_CACHE_RESET** Configures whether or not to reset L1 ichache 1.  
- 0: No effect  
- 1: Reset  
(R/W)

**HP_SYSTEM_L1_IO_CACHE_RESET** Configures whether or not to reset L1 ichache 0.  
- 0: No effect  
- 1: Reset  
(R/W)

## Register 20.17. HP_SYSTEM_HP_SPM_RAM_PWR_CTRLLO_REG (0x003C)

```
31
+---------------------------------------------------------------+
| 1   0 |
| Reset | 
+---------------------------------------------------------------+
```

**HP_SYSTEM_HP_SPM_CLK_FORCE_ON** Configures whether or not to force on HP SPM clock.  
- 0: No effect  
- 1: Force on  
(R/W)