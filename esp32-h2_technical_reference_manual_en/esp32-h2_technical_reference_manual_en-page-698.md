

```markdown
Chapter 27 Random Number Generator (RNG)

When the SAR ADC generates noise, the random number generator obtains 2 bits of entropy per SAR ADC sampling cycle. The SAR ADC sampling cycle is typically 66 kHz, determined by the SAR ADC configuration.

A data sample of 2 GB, which is read from the random number generator at a rate of 5 MHz with only the high-speed ADC being enabled, has been tested using the Dieharder Random Number Testsuite (version 3.31.1). The sample passed all tests.

## 27.4 Programming Procedure

When using the random number generator, make sure at least either the SAR ADC, high-speed ADC¹ is enabled and it is recommended to enable RC_FAST_CLK² to increase the entropy which entry random numbers. Otherwise, pseudo-random numbers will be returned.

*   SAR ADC can be enabled by using the DIG ADC controller. For details, please refer to Chapter 40 ??.
It is recommended to use the following configurations for SAR ADC:

    - Set the sampling channel to collect the internal voltage of the chip
    - Set the controller to use timer-driven continuous sampling mode

*   High-speed ADC is enabled automatically when the Wireless module is enabled.

*   RC_FAST_CLK is enabled by default and it could not be closed.

**Note:**
1.  Note that, when the Wireless module (Thread or BLE) is enabled, the value read from the high-speed ADC can be saturated in some extreme cases, which lowers the entropy. Thus, it is advisable to also enable the SAR ADC as the noise source for the random number generator for such cases.
2.  Enabling RC_FAST_CLK increases the RNG entropy. However, to ensure maximum entropy, it's recommended to always enable an ADC source as well.

When using the random number generator, read the LPPERI_RNG_DATA_REG register multiple times until sufficient random numbers have been generated.

Please ensure that the rate at which the register is read does not exceed the entropy generation frequency described in section 27.3 above.

## 27.5 Register Summary

The abbreviations given in Column Access are explained in Section Access Types for Registers.
| Name | Description | Address | Access |
| :------------------- | :--------------------------------- | :------- | :----- |
| LPPERI_RNG_DATA_REG | Random number data | 0x600B_280C | RO |
```