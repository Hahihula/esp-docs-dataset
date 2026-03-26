

```markdown
Table 10.1-2 – cont’d from previous page

| Code | Source               | Reset Type     | Note                                                                 |
|------|----------------------|----------------|-----------------------------------------------------------------------|
| 0x13 | Power glitch reset   | System Reset   | See Chapter 23 Brown-out Detector                                    |
| 0x14 | Software LP CPU reset| LP CPU Reset   | Triggered by configuring LPPERI_RST_EN_LP_CORE                       |

¹ LP CPU is reset by PMU after chip power-up. To retrieve the correct reset source code (0x01) when the LP CPU runs for the first time, the source code for PMU LP CPU reset (0xOA) will be masked. After the CPU’s first run, clear `LP_CLKRST_LPCORE_RESET_CAUSE_PMU_LP_CPU_MASK` to unmask the 0xOA source code.
```

## 10.1.5 Peripheral Reset

Peripherals can be reset individually by configuring corresponding registers, or globally by Core Reset, System Reset, or Chip Reset.

ESP32-P4 has three groups of peripheral reset registers, prefixed with `HP_SYS_CLKRST`, `LP_CLKRST`, and `LPPERI`. See Section 10.4 Register Summary for detailed information.

## 10.2 Clock

### 10.2.1 Overview

ESP32-P4 clocks are mainly sourced from oscillator (OSC, including Resistor-Capacitor circuit), crystal (XTAL), and PLL circuit, and then processed by the dividers or selectors, which allows most functional modules to select their working clock according to their power consumption and performance requirements. Figure 10.2-1 shows the HP and LP system clock structure, including the main clock path and typical peripheral clock generator circuit. ESP32-P4 has a large number of peripherals, and limited by space, not all peripheral clocks are shown in the figure.
```