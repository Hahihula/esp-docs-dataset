

```markdown
Register 8.74. PCR_DATE_REG (0xOFFC)

PCR_DATE Version control register.
(R/W)
```

## 8.5.2 LP Registers

The addresses in this section are relative to the Low-power Clock/Reset Register (LP_CLKRST) base address. For base address, please refer to Table 5.3-2 in Chapter 5 System and Memory.

Register 8.75. LP_CLKRST_LP_CLK_CONF_REG (0x0000)

```markdown
LP_CLKRST_SLOW_CLK_SEL Configures the source of LP_SLOW_CLK.
0: RC_SLOW_CLK
1: XTAL32K_CLK
2: OSC_SLOW_CLK
3: Invalid
(R/W)
```

```markdown
LP_CLKRST_FAST_CLK_SEL configures the source of LP_FAST_CLK.
0: RC_FAST_CLK
1: XTAL_D2_CLK
(R/W)
```
```