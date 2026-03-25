

```markdown
Note:

1. When the Wi-Fi module is enabled, the high-speed ADC may produce saturated readings in extreme cases, which reduces entropy. To mitigate this, enable the SAR ADC as an additional noise source for the random number generator.

2. Enabling RC_FAST_CLK and asynchronous counters increases the RNG entropy. However, to ensure maximum entropy, always enable the SAR ADC or high-speed ADC as well.
```

When multiple random numbers are required, the value of the `LPPERI_RNG_DATA_SYNC_REG` register can be read continuously. However, when reading the register, ensure that the rate does not exceed the entropy generation rate described in Section 24.3. If multiple entropy sources are configured, it is recommended to not exceed the entropy generation rate of the lowest noise source.
```