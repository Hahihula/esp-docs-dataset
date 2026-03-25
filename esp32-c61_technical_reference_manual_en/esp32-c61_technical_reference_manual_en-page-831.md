

```markdown
LPPEI_RNG_DATA_SYNC_REG register at a maximum rate of 66 kHz to obtain the maximum entropy.

When there is noise coming from the high-speed ADC, the random number generator is fed with a 2-bit entropy in one APB clock cycle, which is normally 80 MHz. Thus, it is advisable to read the LPPEI_RNG_DATA_SYNC_REG register at a maximum rate of 5 MHz to obtain the maximum entropy.

When BUF_CHAIN is enabled, 1 bit of entropy can be obtained in each RC_FAST_CLK cycle.

A data sample of 2 GB, which is read from the random number generator at a rate of 5 MHz with only the high-speed ADC being enabled, has been tested using the Dieharder Random Number Testsuite (version 3.31.1). The sample passed all tests.
```

## 24.4 Programming Procedure

To use the random number generator, set LPPEI_RNG_CK_EN to enable its clock. The clock is automatically enabled when Elliptic Curve Digital Signature Algorithm (ECDSA) is used, regardless of LPPEI_RNG_CK_EN.

When using the random number generator, make sure the entropy source is enabled. Otherwise, pseudo-random numbers will be returned.

- SAR ADC can be enabled by using the DIG ADC controller. For details, please refer to Chapter 33 ADC Controller.
- High-speed ADC is enabled automatically when the Wi-Fi or Bluetooth module is enabled.
- RC_FAST_CLK is always enabled
- Asynchronous counters
    - RTC timer (RTC_TIMER) is enabled by setting the LPPEI_RTC_TIMER_EN field.
    - Ring oscillator (BUF_CHAIN) is enabled by setting the LPPEI_RNG_SAMPLE_ENABLE bit.

Figure 24.3-1. Noise Source

```plaintext
SAR ADC random bit seeds XOR Random Number Generator LPPEI_RNG_DATA_SYNC_REG
High-Speed ADC random bit seeds XOR
RC_FAST_CLK random bit seeds
RTC_TIMER random bit seeds XOR
BUF_CHAIN random bit seeds
```

Espressif Systems
831
ESP32-C61 TRM (Pre-release v0.5)
Submit Documentation Feedback PRELIMINARY
```