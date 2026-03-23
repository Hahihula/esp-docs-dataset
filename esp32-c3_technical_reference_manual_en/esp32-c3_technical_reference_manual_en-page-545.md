

```markdown
## 24.4 Programming Procedure

When using the random number generator, make sure at least either the SAR ADC, high-speed ADC¹, or RC_FAST_CLK² is enabled. Otherwise, pseudo-random numbers will be returned.

- SAR ADC can be enabled by using the DIG ADC controller. For details, please refer to Chapter 34 On-Chip Sensor and Analog Signal Processing.
- High-speed ADC is enabled automatically when the Wi-Fi or Bluetooth modules is enabled.
- RC_FAST_CLK is enabled by setting the RTC_CNTL_DIG_FOSC_EN bit in the RTC_CNTL_CLK_CONF_REG register.

**Note:**
1. Note that, when the Wi-Fi module is enabled, the value read from the high-speed ADC can be saturated in some extreme cases, which lowers the entropy. Thus, it is advisable to also enable the SAR ADC as the noise source for the random number generator for such cases.
2. Enabling RC_FAST_CLK increases the RNG entropy. However, to ensure maximum entropy, it's recommended to always enable an ADC source as well.

When using the random number generator, read the RNG_DATA_REG register multiple times until sufficient random numbers have been generated. Ensure the rate at which the register is read does not exceed the frequencies described in section 24.3 above.
```

```markdown
## 24.5 Register Summary

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name             | Description           | Address     | Access |
|------------------|-----------------------|-------------|--------|
| RNG_DATA_REG     | Random number data    | 0x6002_60B0 | RO     |
```