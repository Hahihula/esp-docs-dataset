

```markdown
Matrix > Section 11.2 Terminology


Each interrupt source can be configured by a common set of registers that are described in Section Interrupt Configuration Registers. The specific registers can be found in Section 15.8 Register Summary.


## 15.7 Programming Procedures

### 15.7.1 Timer as a Simple Clock

1. Configure the time-base counter
   - Select clock source by setting or clearing `PCR_TGO_TIMER_CLK_SEL` field.
   - Configure the 16-bit prescaler by setting `TIMG_TO_DIVIDER`.
   - Configure the timer direction by setting or clearing `TIMG_TO_INCREASE`.
   - Set the timer's starting value by writing the starting value to `TIMG_TO_LOAD_LO` and `TIMG_TO_LOAD_HI`, then reloading it into the timer by writing any value to `TIMG_TOLOAD_REG`.

2. Start the timer by setting `TIMG_TO_EN`.

3. Get the timer's current value.
   - Write any value to `TIMG_TOUPDATE_REG` to latch the timer's current value.
   - Wait until `TIMG_TOUPDATE_REG` is cleared by hardware.
   - Read the latched timer value from `TIMG_TOLO_REG` and `TIMG_TOHI_REG`.

### 15.7.2 Timer as One-shot Alarm

1. Configure the time-base counter following step 1 of Section 15.7.1.

2. Configure the alarm.
   - Configure the alarm value by setting `TIMG_TOALARMLO_REG` and `TIMG_TOALARMHI_REG`.
   - Enable interrupt by setting `TIMG_TO_INT_ENA`.

3. Disable auto reload by clearing `TIMG_TO_AUTORELOAD`.

4. Start the alarm by setting `TIMG_TO_ALARM_EN`.

5. Handle the alarm interrupt.
   - Clear the interrupt by setting the timer's corresponding bit in `TIMG_TO_INT_CLR`.
   - Disable the timer by clearing `TIMG_TO_EN`.


### 15.7.3 Timer as Periodic Alarm by APB

1. Configure the time-base counter following step 1 in Section 15.7.1.

2. Configure the alarm following step 2 in Section 15.7.2.
```