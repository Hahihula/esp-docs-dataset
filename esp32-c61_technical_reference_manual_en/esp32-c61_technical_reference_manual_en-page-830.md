

```markdown
Chapter 24 Random Number Generator (RNG)

GoBack

Chapter 24

Random Number Generator (RNG)

24.1 Introduction

The ESP32-C61 contains a true random number generator, which generates 32-bit random numbers that can be used for cryptographical operations, among other things.

24.2 Features

The random number generator in ESP32-C61 generates true random numbers, meaning they are derived from a physical process rather than an algorithm. Each number within the specified range has an equal probability of occurrence.

24.3 Functional Description

Every 32-bit value that the system reads from the LPPERI_RNG_DATA_SYNC_REG register of the random number generator is a true random number. These true random numbers are generated based on the thermal noise in the system, the asynchronous clock mismatch, and the asynchronous counter.

- Thermal noise comes from the high-speed ADC, or SAR ADC, or both. Whenever the high-speed ADC or SAR ADC is enabled, bit streams will be generated and fed into the random number generator through an XOR logic gate as random seeds.
- RC_FAST_CLK is an asynchronous clock source source that can generate metastability in the circuit. This metastability can also be used as a random number seed ² to feed into the random number generator.
- Asynchronous counters count using an asynchronous clock source. The asynchronous clock source generates circuit metastability, which can be used as a random number seed to feed into the random number generator. There are two types of asynchronous counters:

    - On-chip RTC Timer (RTC_TIMER): The counter directly counts using the on-chip RTC timer. The count value is fed into the random number generator as a random number seed after applying XOR logic.
    - Ring oscillator (BUF_CHAIN): The counter counts based on the ring oscillator, formed by connecting buffer cells end-to-end. The count value derived from this oscillator is fed into the random number generator as a random number seed after applying XOR logic.

These two types of asynchronous counters can work independently or in combination.

When there is noise coming from the SAR ADC, the random number generator is fed with a 2-bit entropy in one clock cycle (configurable, normally 66 kHz). Thus, it is advisable to read the
```