

```markdown
## Register 9.69. PCR_CTRL_32K_CONF_REG (0x0130)

PCR_32K_SEL Configures the 32 kHz clock for TIMER_GROUP.
- 0: XTAL32K_CLK
- 1: OSC_SLOW_CLK
- 2: RC_SLOW_CLK
- 3: RC_FAST_CLK
(R/W)

PCR_FOSC_TICK_NUM Configure the division factor for the RC_FAST_CLK to enter the calibration module. (Effective when PCR_32K_SEL is set to 4).
(R/W)
```

```markdown
## Register 9.70. PCR_SEC_CONF_REG (0x013C)

PCR_SEC_CLK_SEL Configures the clock source for the External Memory Encryption and Decryption module.
- 0 (default): XTAL_CLK
- 1: RC_FAST_CLK
- 2: PLL_F48OM_CLK
- 3: No clock source
(R/W)

PCR_SEC_RST_EN Configures whether or not to reset the SEC.
- 0: Not reset
- 1: Reset
(R/W)
```