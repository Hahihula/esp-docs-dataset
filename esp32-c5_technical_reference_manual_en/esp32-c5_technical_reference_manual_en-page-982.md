

```markdown
Chapter 30 Random Number Generator (RNG)

GoBack

Chapter 30

Random Number Generator (RNG)

30.1 Introduction

The ESP32-C5 contains a true random number generator, which generates 32-bit random numbers that can be used for cryptographical operations, among other things.

30.2 Features

The random number generator in ESP32-C5 generates true random numbers, which means random numbers derived from a physical process, rather than by means of an algorithm. All generated random numbers have an equal probability of appearing within a specific range.

30.3 Functional Description

Every 32-bit value read from the LPPERI_RNG_DATA_SYNC_REG register of the random number generator is a true random number. These true random numbers are generated based on the thermal noise in the system, the asynchronous clock mismatch, and the asynchronous counter.

- Thermal noise comes from the high-speed ADC, or SAR ADC, or both. Whenever the high-speed ADC or SAR ADC is enabled, bit streams will be generated and fed into the random number generator through an XOR logic gate as random seeds.
- RC_FAST_CLK is an asynchronous clock source that can generate metastability in the circuit. This metastability can be used as a random number entropy to feed into the random number generator.
- Asynchronous counters count using an asynchronous clock source. The asynchronous clock source generates circuit metastability, which can be used as a random number seed to feed into the random number generator. There are two types of asynchronous counters:

  - On-chip RTC Timer (RTC_TIMER): The counter directly counts using the on-chip RTC timer. The count value is fed into the random number generator as a random number seed after applying XOR logic.
  - Ring buffer (BUF_CHAIN) as the noise source.

These two types of asynchronous counters can work independently or in combination.

Note:
For limitations of particular noise sources, please check notes in Section Programming Procedures.
```