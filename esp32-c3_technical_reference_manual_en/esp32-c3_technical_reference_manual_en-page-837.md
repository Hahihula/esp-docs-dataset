

```markdown
Register 32.2. LEDC_CHn_CONF1_REG (n: 0-5) (0x000C+20*n)

| 31 | 30 | 29           | 28               | 27                 | 26                   | 25                  | 24                    | 23                     | 22                      | 21                       | 20         | 19          | 18              | 17             | 16            | 15           | 14        | 13       | 12      | 11     | 10   | 9    | 8   | 7  | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|--------------|-----------------|-------------------|---------------------|--------------------|-----------------------|------------------------|-------------------------|--------------------------|------------|-------------|----------------|---------------|---------------|---------------|------------|-----------|--------|------|------|----|----|---|---|---|---|---|---|---|---|
| 0   | 1  |              |                 |                   |                     |                    |                       |                        |                         |                          |            |             |                |               |               |               |            |           |        |      |      |    |    |   |   |   |   |   |   |   |   |
|     |    |              |                 |                   |                     |                    |                       |                        |                         |                          | OxO         |             |                |               |               |               |            |           |        |      |      |    |    |   |   |   |   |   |   |   |   |
| Reset|

LEDC_DUTY_SCALE_CHn (R/W)
This field configures the step size of the duty cycle change during fading.

LEDC_DUTY_CYCLE_CHn (R/W)
The duty will change every LEDC_DUTY_CYCLE_CHn cycle on channel n. (R/W)

LEDC_DUTY_NUM_CHn (R/W)
This field controls the number of times the duty cycle will be changed.

LEDC_DUTY_INC_CHn This bit determines whether the duty cycle of the output signal on channel n increases or decreases. 1: Increase; 0: Decrease. (R/W)

LEDC_DUTY_START_CHn If this bit is set to 1, other configured fields in LEDC_CHn_CONF1_REG will take effect upon the next timer overflow. (R/W/SC)

Register 32.3. LEDC_CONF_REG (0x00DO)

| 31 | 30 | ... | reserved | ... | 2 | 1 | 0 |
|-----|----|-----|----------|-----|---|---|---|
| 0   | 0  | 0   |          |     |   |   |   |
| Reset|

LEDC_APB_CLK_SEL This field is used to select the common clock source for all the 4 timers.
1: APB_CLK; 2: RC_FAST_CLK; 3: XTAL_CLK. (R/W)

LEDC_CLK_EN This bit is used to control the clock.
1: Force clock on for register. 0: Support clock only when application writes registers. (R/W)
```