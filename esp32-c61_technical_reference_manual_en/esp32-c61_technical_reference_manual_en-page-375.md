

```markdown
Register 7.55. PCR_CTRL_32K_CONF_REG (0x010C)

PCR_32K_SEL Configures the 32 kHz clock for TIMER_GROUP.
0: reserved
1: XTAL32K_CLK
2: OSC_SLOW_CLK
3: RC_SLOW_CLK
4: Clock from RC_FAST_CLK after division by PCR_FOSC_TICK_NUM
(R/W)

PCR_FOSC_TICK_NUM Configure the division factor for the RC_FAST_CLK to enter the calibration module. (Effective when PCR_32K_SEL is set to 4).
(R/W)
```

```markdown
Register 7.56. PCR_SEC_CONF_REG (0x0118)

PCR_SEC_CLK_SEL Configures the clock source for the External Memory Encryption and Decryption module.
0 (default): XTAL_CLK
1: RC_FAST_CLK
2: PLL_F480M_CLK
(R/W)

PCR_SEC_RST_EN Configures whether or not to reset the SEC.
0: Not reset
1: Reset
(R/W)
```