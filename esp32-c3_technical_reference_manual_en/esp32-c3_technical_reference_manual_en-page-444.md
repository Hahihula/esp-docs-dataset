

```markdown
Register 16.19. SYSTEM_CLOCK_GATE_REG (0x0054)

SYSTEM_CLK_EN Set this bit to enable the system clock. (R/W)


Register 16.20. SYSTEM_DATE_REG (0x0FFC)

SYSTEM_DATE Version control register. (R/W)


The addresses below are relative to the base address of apb control provided in Table 3.3-3 in Chapter 3
System and Memory.

Register 16.21. SYSCON_CLKGATE_FORCE_ON_REG (0x00A4)

SYSCON_ROM_CLKGATE_FORCE_ON Set 1 to configure the ROM clock gate to be always on; Set
0 to configure the clock gate to turn on automatically when ROM is accessed and turn off auto-
matically when ROM is not accessed. (R/W)

SYSCON_SRAM_CLKGATE_FORCE_ON Set 1 to configure the SRAM clock gate to be always on;
Set 0 to configure the clock gate to turn on automatically when SRAM is accessed and turn off
automatically when SRAM is not accessed. (R/W)
```