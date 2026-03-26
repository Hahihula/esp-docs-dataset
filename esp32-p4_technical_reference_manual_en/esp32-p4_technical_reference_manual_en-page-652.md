

# 10.5 Registers

## 10.5.1 Reset and Clock (HP_SYS_CLKRST) Registers

The addresses in this section are relative to HP_SYS_CLKRST base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

### Register 10.1. HP_SYS_CLKRST_CLK_ENO_REG (0x0000)

```
(reserved)
HP_SYS_CLKRST_CLK_EN

31
------------------------------------------------------------> 0

0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1 Reset
```

**HP_SYS_CLKRST_CLK_EN** Configures register clock gating.

- 0: Support clock only when application writes registers
- 1: Force on clock gating for registers  
(R/W)