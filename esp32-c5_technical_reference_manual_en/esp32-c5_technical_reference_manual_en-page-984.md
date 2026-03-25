

```markdown
Chapter 30 Random Number Generator (RNG)  
GoBack

cases, which lowers the entropy. Thus, it is advisable to also enable the SAR ADC as the noise source for the random number generator for such cases.

2. Enabling RC_FAST_CLK and asynchronous counters increases the RNG entropy. However, to ensure maximum entropy, it's recommended to always enable the SAR ADC or high-speed ADC as well.

Read the LPPERI_RNG_DATA_SYNC_REG register multiple times until sufficient random numbers have been generated. Ensure the rate at which the register is read does not exceed the frequencies described in Section 30.3 above.
```