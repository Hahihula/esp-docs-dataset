

```markdown
Chapter 33 Random Number Generator (RNG)

When there is noise coming from the SAR ADC, the random number generator is fed with a 1-bit entropy in one clock cycle of RC_FAST_CLK, which is generated from an internal RC oscillator (see Chapter 10 Reset and Clock for details). Thus, it is advisable to read the LPSYSREG_RNG_DATA_REG register at a maximum rate of 1 MHz to obtain the maximum entropy.

33.4 Programming Procedure

When using the random number generator, make sure at least either the SAR ADC or RC_FAST_CLK is enabled. Otherwise, pseudo-random numbers will be returned.

*   For SAR ADC, please refer to Chapter 62 ADC Controller (ADC).
*   RC_FAST_CLK is enabled by setting the PMU_HP_SLEEP_XPD_FOSC_CLK bit in the PMU_HP_SLEEP_LP_CK_POWER_REG register. Please refer to the Note about the RC_FAST_CLK.
*   RC_FAST_CLK is gated by setting the LPPERI_CK_EN_RNG bit in the LPPERI_CLK_EN_REG register.
*   The BUF_CHAIN can be enabled by setting the RNG_CFG_REG register's RNG_SAMPLE_ENABLE bit.

Note:
Enabling RC_FAST_CLK increases the RNG entropy. However, to ensure maximum entropy, it's recommended to always enable an ADC source as well.

When using the random number generator, read the LPSYSREG_RNG_DATA_REG register multiple times until sufficient random numbers have been generated. Ensure the rate at which the register is read does not exceed the frequencies described in section 33.3 above.
```