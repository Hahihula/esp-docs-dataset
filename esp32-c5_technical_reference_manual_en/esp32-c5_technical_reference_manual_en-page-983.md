

```markdown
Figure 30.3-1. Noise Source

When there is noise coming from the SAR ADC, the random number generator is fed with a 2-bit entropy in one clock cycle of RC_FAST_CLK, which is generated from an internal RC oscillator (see Chapter 9 Reset and Clock for details). Thus, it is advisable to read the LPPERI_RNG_DATA_SYNC_REG register at a maximum rate of 1 MHz to obtain the maximum entropy.

When there is noise coming from the high-speed ADC, the random number generator is fed with a 2-bit entropy in one APB clock cycle, which is normally 80 MHz. Thus, it is advisable to read the LPPERI_RNG_DATA_SYNC_REG register at a maximum rate of 5 MHz to obtain the maximum entropy.

A data sample of 2 GB, which is read from the random number generator at a rate of 5 MHz with only the high-speed ADC being enabled, has been tested using the Dieharder Random Number Testsuite (version 3.31.1). The sample passed all tests.

## 30.4 Programming Procedure

To use the random number generator, set LPPERI_RNG_CK_EN to enable its clock. The clock is automatically enabled when Elliptic Curve Digital Signature Algorithm (ECDSA) is used, regardless of LPPERI_RNG_CK_EN.

When using the random number generator, ensure the entropy source is enabled. Otherwise, pseudo-random numbers will be returned.

*   SAR ADC can be enabled by using the DIG ADC controller. For details, please refer to Chapter 46 ADC Controller.
*   High-speed ADC is enabled automatically when the Wi-Fi or Bluetooth module is enabled.
*   RC_FAST_CLK is always enabled
*   Asynchronous counters

    -   RTC timer (RTC_TIMER) is enabled by setting the LPPERI_RTC_TIMER_EN field.
    -   Ring buffer (BUF_CHAIN) is enabled by setting the LPPERI_RNG_SAMPLE_ENABLE bit.

Note:
1.  When the Wi-Fi module is enabled, the value read from the high-speed ADC can be saturated in some extreme
```