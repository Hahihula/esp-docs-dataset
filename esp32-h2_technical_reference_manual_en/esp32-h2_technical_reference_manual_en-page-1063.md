

```markdown
Chapter 36 Motor Control PWM (MCPWM) GoBack

36.3.1.5 Capture Module

Figure 36.3-5. Capture Module

Configuration options:
* Select the edge polarity and prescale the capture input
* Set up a software-triggered capture
* Configure the capture timer’s sync trigger and sync phase
* Software syncs the capture timer

36.3.1.6 ETM Module

Figure 36.3-6. ETM Module

Configuration options:
* Each event and task can be enabled independently. When an event is not enabled, the corresponding event will not be generated. When a task is not enabled, the corresponding task will not be responded to.

36.3.2 PWM Timer Module

MCPWM has three PWM timer modules. Any of them can determine the necessary event timing for any of the three PWM operator modules. By using the synchronization signals from the GPIO matrix, built-in synchronization logic allows multiple PWM timer modules in this MCPWM peripheral to work together as a system.

36.3.2.1 Configurations of the PWM Timer Module

Users can configure the following functions of the PWM timer module:
* Control how often events occur by specifying the PWM timer frequency or period
* Configure a particular PWM timer to synchronize with other PWM timers or modules
* Get a PWM timer in phase with other PWM timers or modules.
```