

```markdown
Chapter 41 Motor Control PWM (MCPWM)                                                                 GoBack


# 41.3 Modules

## 41.3.1 Overview

The key modules in each MCPWM are timer module, operator module, fault detection module, capture module, and ETM module. See their functions in the following sections.

### 41.3.1.1 Timer Module

![Figure 41.3-1. Timer Module](image)

This module contains a timer, which can count at a specified period. It can work in Count-Up Mode, Count-Down Mode, or Count-Up-Down Mode. It supports different synchronization input sources (a total of seven optional input sources) for reloading the count value and direction, allowing synchronization among multiple timers. Furthermore, it provides synchronization output options (a total of four optional output sources) for use by other timers.

The timerx status in the figure represents the timer status output by the timer module, such as the counting mode, and count value equal to zero or period.

### 41.3.1.2 Operator Module

![Figure 41.3-2. Operator Module](image)

A PWM operator contains a PWM generator, a dead time generator, and a PWM carrier module. Their functions are shown in Table 41.3-1.
```