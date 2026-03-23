

```markdown
Register 8.58. INTERRUPT_COREO_CPU_INT_EIP_STATUS_REG (0x0110)

31
+-----------------------------------------------+
|                                           |
|                                           | 0
+-----------------------------------------------+
|                                           | Reset
+-----------------------------------------------+

INTERRUPT_COREO_CPU_INT_EIP_STATUS   Store the pending status of CPU interrupts. For more information about how to use this register, see Chapter 1 ESP-RISC-V CPU. (RO)

Register 8.59. INTERRUPT_COREO_CPU_INT_PRI_n_REG (n: 1 - 31)(0x0118 + 0x4*n)

(reserved)
31
+-----------------------------------------------+
|                                           |
|                                           | Reset
+-----------------------------------------------+

INTERRUPT_COREO_CPU_PRI_n_MAP   Set the priority for CPU interrupt n. The priority here can be 1 (lowest) ~ 15 (highest). For more information about how to use this register, see Chapter 1 ESP-RISC-V CPU. (R/W)
```