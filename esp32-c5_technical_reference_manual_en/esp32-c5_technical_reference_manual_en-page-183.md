

```markdown
Register 4.27. LPPERI_CPU_REG (0x000C)

LPPI_LPCORE_DGGM_UNAVAILABLE Configures the LP CPU state.
O: LP CPU can connect to JTAG
1: LP CPU is unavailable and cannot connect to JTAG
(R/W)
```

```markdown
Register 4.28. LPPERI_INTERRUPT_SOURCE_REG (0x0020)

LPPI_LP_INTERRUPT_SOURCE Represents the LP interrupt source.

Bit 5: PMU_LP_INT
Bit 4: Reserved
Bit 3: RTC_TIMER_LP_INT
Bit 2: LP_UART_INT
Bit 1: LP_I2C_INT
Bit 0: LP_IO_INT
(RO)
```