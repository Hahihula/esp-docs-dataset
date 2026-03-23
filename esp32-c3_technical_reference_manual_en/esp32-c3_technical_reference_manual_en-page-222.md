

```markdown
Note:
1. Each power domain has its own power controller. For a complete list of all the available power controllers controlling different power domains, please refer to Section 9.4.1.
2. For a complete list of all the available wakeup sources, please refer to Table 9.4-2.

## 9.3.2 Low-Power Clocks

In general, ESP32-C3 powers down its external main crystal oscillator XTAL_CLK and PLL to reduce power consumption when working in low-power modes. During this time, the chip's low-power clocks remain on to provide clocks to low power domains, such as the power management unit.

Figure 9.3-3. RTC Clocks
```