

```markdown
Register 7.61. PCR_ETM_CONF_REG (0x013C)

PCR_ETM_CLK_EN   configures whether or not to enable ETM clock.
O: Not enable
1: Enable
(R/W)

PCR_ETM_RST_EN   Configures whether or not to reset ETM.
O: Reset
1: Not reset
(R/W)

PCR_ETM_READY    Represents whether or not ETM is released from reset.
O: Not released
1: Released
(RO)
```

```markdown
Register 7.62. PCR_DATE_REG (0x0FFC)

PCR_DATE         Version control register. (R/W)
```

## 7.5.2 LP System Clock Registers

The addresses of the last two registers with the LPPERI prefix in this section are relative to the Low-power Peripheral Register (LPPERI) base address. The addresses of the third and fourth to last registers with the LP_AON prefix in this section are relative to the Low-power Always-on Register (LP_AON) base address. The other addresses in this section are relative to the Low-power Clock/Reset Register (LP_CLKRST) base address. For base address, please refer to Table 4.3-2 in Chapter 4 System and Memory.
```