

# 20.5 Registers

## 20.5.1 HP Registers

The addresses in this section are relative to HP System Registers base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

### Register 20.1. HP_SYSTEM_VER_DATE_REG (0x0000)

```
HP_SYSTEM_REG_VER_DATE
31
0x20230519 Reset
```

**HP_SYSTEM_REG_VER_DATE** Version control register. (R/W)

---

### Register 20.2. HP_SYSTEM_CLK_EN_REG (0x0004)

```
(reserved)
31
0x00000000 Reset
```

**HP_SYSTEM_CLK_EN** Configures whether or not to enable system clock.

- 0: Disable
- 1: Enable

(R/W)