

```markdown
Chapter 8 Interrupt Matrix (INTERRUPT)  
GoBack

Register 8.55. INTERRUPT_COREO_CPU_INT_ENABLE_REG (0x0104)

31 0 Reset  
[Horizontal bar representation of register bits]  

INTERRUPT_COREO_CPU_INT_ENABLE Writing 1 to the bit here enables its corresponding CPU interrupt. For more information about how to use this register, see Chapter 1 ESP-RISC-V CPU. (R/W)

Register 8.56. INTERRUPT_COREO_CPU_INT_TYPE_REG (0x0108)

31 0 Reset  
[Horizontal bar representation of register bits]  

INTERRUPT_COREO_CPU_INT_TYPE Configure CPU interrupt type. 0: level-triggered; 1: edge-triggered. For more information about how to use this register, see Chapter 1 ESP-RISC-V CPU. (R/W)

Register 8.57. INTERRUPT_COREO_CPU_INT_CLEAR_REG (0x010C)

31 0 Reset  
[Horizontal bar representation of register bits]  

INTERRUPT_COREO_CPU_INT_CLEAR Writing 1 to the bit here clears its corresponding CPU interrupt. For more information about how to use this register, see Chapter 1 ESP-RISC-V CPU. (R/W)
```