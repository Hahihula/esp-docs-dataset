

```markdown
## 36.3.2.3 Shadow Register of PWM Timer

The PWM timer's period register and the PWM timer's clock prescaler register have shadow registers. The shadow registers can back up the values that are about to be written to the valid registers. It also supports to write the values saved into the active register at a specific moment of hardware synchronization. The functionality of both register types is as follows:

* Active Register: Directly responsible for controlling all actions performed by hardware.
* Shadow Register: Acts as a temporary buffer for a value to be written to the active register. At a specific, user-configured point in time, the value saved in the shadow register is copied to the active register. Before this happens, the content of the shadow register has no direct effect on the controlled hardware. This helps to prevent erroneous operation of the hardware, which may happen when a register is asynchronously modified by software. Both the shadow register and the active register have the same memory address. The software always writes into, or reads from the shadow register.

The moment of updating the clock prescaler's active register is at the time when the timer starts operating. When `MCPWM_GLOBAL_UP_EN` is set to 1, the moment of updating the period active register can be selected by the following ways:

- By configuring the update method register `MCPWM_TIMERx_PERIOD_UPMETHOD` to 0, the update will start immediately.
- By configuring the update method register `MCPWM_TIMERx_PERIOD_UPMETHOD` to 1, the update can start when the PWM timer is equal to zero.
- By configuring the update method register `MCPWM_TIMERx_PERIOD_UPMETHOD` to 2, the update can start when the PWM timer is synchronized.
- By configuring the update method register `MCPWM_TIMERx_PERIOD_UPMETHOD` to 3, the update can start when the PWM timer is equal to zero or is synchronized.
- Software can also trigger a globally forced update bit `MCPWM_GLOBAL_FORCE_UP` which will prompt all registers in the module to be updated according to shadow registers.

## 36.3.2.4 PWM Timer Synchronization and Phase Locking

The PWM modules adopt a flexible synchronization method. Each PWM timer has a synchronization input and a synchronization output. The synchronization input can be selected from three synchronization outputs and three synchronization signals from the GPIO matrix. The synchronization output can be generated from the synchronization input signal, when the PWM timer's value is equal to period or zero, or software synchronization. Thus, the PWM timers can be chained together with their phase locked. During synchronization, the PWM timer clock prescaler will reset its counter in order to synchronize the PWM timer clock.

## 36.3.3 PWM Operator Module

The PWM Operator module has the following functions:

* Generates a PWM signal pair, based on timing references obtained from the corresponding PWM timer.
* Each signal out of the PWM signal pair includes a specific pattern of dead time.
```