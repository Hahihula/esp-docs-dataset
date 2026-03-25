

# Chapter 9 Interrupt Matrix (INTMTX)

Register 9.59. INTMTX_COREO_INTERRUPT_REG_DATE_REG (0x07FC)

| Bit Range | Value   |
|-----------|---------|
| 31        | 28      | 27     | ...    | 0       |
|           |         | O O O  |        | Reset   |
|           |         |        |        | 0x2209150 |

INTMTX_COREO_INTERRUPT_REG_DATE Version control register (R/W)

## 9.7.2 Interrupt Priority Registers

The addresses in this section are relative to the interrupt priority base address provided in Table 4.3-2 in Chapter 4 System and Memory.

Register 9.60. INTPRI_COREO_CPU_INT_ENABLE_REG (0x0000)

| Bit Range | Value |
|-----------|-------|
| 31        | ...   | 0     |
|           |       | Reset |

INTPRI_COREO_CPU_INT_ENABLE Configures whether to enable the corresponding CPU interrupt.

- O: Not enable
- 1: Enable

For more information about how to use this register, see Chapter 1 ESP-RISC-V CPU > Section 1.6 Interrupt Controller.
(R/W)