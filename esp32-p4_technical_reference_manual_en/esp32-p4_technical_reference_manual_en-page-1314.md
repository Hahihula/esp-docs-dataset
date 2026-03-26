

```markdown
Chapter 20 System Registers (SYSREG)

Register 20.88. LP_SYSTEM_SYS_CTRL_REG (0x0008)

Continued from the previous page...

LP_SYSTEM_ANA_FIB Represents analog FIB state.
bit-0: Unused
bit-1: Analog BOD enable
bit-2: Analog SWD enable
bit-3: Unused
bit-4: Unused
bit-5: Unused
bit-6: Unused
bit-7: Unused
(RO)

LP_SYSTEM_LP_FIB_SEL Configures FIB control source select.
bit-0: Unused
bit-1: BOD enable control select. 0: Controlled by software, 1: Controlled by analog
bit-2: SWD enable control select. 0: Controlled by software, 1: Controlled by analog
bit-3: Unused
bit-4: Unused
bit-5: Unused
bit-6: Unused
bit-7: Unused
(R/W)

LP_SYSTEM_LP_CORE_ETM_WAKEUP_FLAG_CLR Write    1        to       clear
LP_SYSTEM_LP_CORE_ETM_WAKEUP_FLAG. (WT)

LP_SYSTEM_LP_CORE_ETM_WAKEUP_FLAG Represents ETM task of ULP wakeup. (R/WTC/SS)

LP_SYSTEM_SYSTIMER_STALL_SEL Configures whether the LP systimer_stall signal is from HP CPU0 or HP CPU1.
0: From HP CPU0
1: From HP CPU1
(R/W)
```