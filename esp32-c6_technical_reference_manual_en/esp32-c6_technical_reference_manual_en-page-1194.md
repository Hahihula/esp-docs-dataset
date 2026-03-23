

# 36.3 Modules

## 36.3.1 Overview

This section lists the configuration parameters of key modules. For information on adjusting a specific parameter, e.g. synchronization source of PWM timer, please refer to Section 36.3.2 for details.

### 36.3.1.1 Prescaler Module

Figure 36.3-1. Prescaler Module

Configuration option:
* Scale the PWM_CORE_CLK.

### 36.3.1.2 Timer Module

Figure 36.3-2. Timer Module

Configuration options:
* Configure the PWM timer frequency or period.
* Configure the working mode for the timer:
    - Count-Up Mode: for asymmetric PWM outputs
    - Count-Down Mode: for asymmetric PWM outputs
    - Count-Up-Down Mode: for symmetric PWM outputs
* Configure the reloading phase (including the value and the direction) used during software and hardware synchronization.
* Synchronize the PWM timers with each other. Either hardware or software synchronization may be used.
* Configure the source of the PWM timer’s the synchronization input to one of the seven sources below:
    - The three PWM timer’s synchronization outputs.
    - Three synchronization signals from the GPIO matrix: `PWMn_SYNC0_IN`, `PWMn_SYNC1_IN`, `PWMn_SYNC2_IN`.