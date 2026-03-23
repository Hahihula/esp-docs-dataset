

```markdown
GoBack

Chapter 8 Interrupt Matrix (INTERRUPT)

Register 8.60. INTERRUPT_COREO_CPU_INT_THRESH_REG (0x0194)

31 | 4 | 3 | 0
+---+-----+----+
|   |     |    |
|   | Reset|
|   |       |

INTERRUPT_COREO_CPU_INT_THRESH Set threshold for interrupt assertion to CPU. Only when the interrupt priority is equal to or higher than this threshold, CPU will respond to this interrupt. For more information about how to use this register, see Chapter 1 ESP-RISC-V CPU. (R/W)

Register 8.61. INTERRUPT_COREO_INTERRUPT_DATE_REG (0x07FC)

31 | 28 | 27 | 0
+---+-----+----+
|   |     |    |
|   | Reset|
|   |       |

INTERRUPT_COREO_INTERRUPT_DATE Version control register. (R/W)
```