

```markdown
## 32.3 Functional Description

### 32.3.1 Architecture

Figure 32.2-1 shows the architecture of the LED PWM Controller.

The four timers can be independently configured (i.e. configurable clock divider, and counter overflow value) and each internally maintains a timebase counter (i.e. a counter that counts on cycles of a reference clock). Each PWM generator selects one of the timers and uses the timer’s counter value as a reference to generate its PWM signal.

Figure 32.3-1 illustrates the main functional blocks of the timer and the PWM generator.

![Figure 32.3-1. LED PWM Generator Diagram](image_path_if_available)

### 32.3.2 Timers

Each timer in LED PWM Controller internally maintains a timebase counter. Referring to Figure 32.3-1, this clock signal used by the timebase counter is named ref_pulsex. All timers use the same clock source LEDC_CLKx, which is then passed through a clock divider to generate ref_pulsex for the counter.

#### 32.3.2.1 Clock Source

LED PWM registers configured by software are clocked by APB_CLK. For more information about APB_CLK, see Chapter 6 Reset and Clock. To use the LED PWM peripheral, the APB_CLK signal to the LED PWM has to be enabled. The APB_CLK signal to LED PWM can be enabled by setting the SYSTEM_LEDC_CLK_EN field in the register SYSTEM_PERIP_CLK_ENO_REG and be reset via software by setting the SYSTEM_LEDC_RST field in the register SYSTEM_PERIP_RST_ENO_REG. For more information, please refer to Table 16.3-1 in Chapter 16 System Registers (SYSREG).

Timers in the LED PWM Controller choose their common clock source from one of the following clock signals: APB_CLK, RC_FAST_CLK and XTAL_CLK (see Chapter 6 Reset and Clock for more details about each clock signal). The procedure for selecting a clock source signal for LEDC_CLKx is described below:
```