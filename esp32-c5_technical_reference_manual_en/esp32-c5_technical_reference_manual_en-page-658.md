

```markdown
Register 13.55. PMU_LP_CPU_PWR1_REG (0x0184)

PMU_LP_CPU_WAKEUP_EN Configures the wake-up source for LP CPU. For details please refer to Chapter 4 Low-Power CPU > Table 4.9-1 Wake Sources. (R/W)

PMU_LP_CPU_SLEEP_REQ Configures whether to put LP CPU into sleep.
O: Do not put LP CPU into sleep.
1: Put LP CPU into sleep.
(WT)
```

```markdown
Register 13.56. PMU_HP_LP_CPU_COMM_REG (0x0188)

PMU_LP_TRIGGER_HP When LP CPU configures this register to 1, the chip is woken up. (WT)

PMU_HP_TRIGGER_LP When HP CPU configures this register to 1, LP CPU is woken up. (WT)
```

```markdown
Register 13.57. PMU_DATE_REG (0x01A8)

PMU_PMU_DATE Version control register. (R/W)
```

## 13.10.2 Always-on Registers

The addresses in this section are relative to the Always-on registers base address provided in Table 6.3-2 in Chapter 6 System and Memory.
```