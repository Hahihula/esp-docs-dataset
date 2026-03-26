

```markdown
Chapter 33 Random Number Generator (RNG) GoBack


## 33.6 Registers

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

### Register 33.1. LPSYSREG_RNG_DATA_REG (0x5011_01A4)

LPSYSREG_RNG_DATA Random number source. (RO)


### Register 33.2. RNG_CFG_REG (0x5012_6000)
```
| Bit | Field Name           | Description                                                                 |
|-----|----------------------|-----------------------------------------------------------------------------|
| 31  |                     |                                                                             |
|     |                      | Reset                                                                       |
|     | 0x00000000           |                                                                             |

RNG_SAMPLE_ENABLE Configures whether to enable the RNG asynchronous clock noise source.
- 1: Enable
- 0: Disable
(R/W)

RNG_TIMER_PSCALE Represents the prescale factor of the RNG internal timer. (R/W)

RNG_RTC_TIMER_EN Configures whether to enable the RNG internal timer.
- 1: Enable and use the counter value of this timer when generating random numbers.
- 0: Disable the timer.
(R/W)
```