

```markdown
Register 3.27. LPPERI_CPU_REG (0x000C)

LPPERI_LPCORE_DBGΜ_UNAVAILABLE Configures the LP CPU state.
O: LP CPU can connect to JTAG
1: LP CPU is unavailable and cannot connect to JTAG
(R/W)
```

```markdown
Register 3.28. LPPERI_INTERRUPT_SOURCE_REG (0x0020)

LPPERI_LP_INTERRUPT_SOURCE Represents the LP interrupt source.

Bit 5: PMU_LP_INT
Bit 4: Reserved
Bit 3: RTC_Timer_LP_INT
Bit 2: LP_UART_INT
Bit 1: LP_I2C_INT
Bit 0: LP_IO_INT
(RO)
```