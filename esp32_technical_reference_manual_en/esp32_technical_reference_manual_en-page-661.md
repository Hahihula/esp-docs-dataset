**Title: Chapter 29 Motor Control PWM (MCPWM)**

**GoBack**

---

### PWM Signal Generation

The PWM generator submodule controls the behavior of outputs PWM<sub>X</sub>A and PWM<sub>X</sub>B when a particular timing event occurs. The timing events are further qualified by the PWM timer’s counting direction (up or down). Knowing the counting direction, the submodule may then perform an independent action at each stage of the PWM timer counting up or down.

The following actions may be configured on outputs PWM<sub>X</sub>A and PWM<sub>X</sub>B:

- **Set High:** Set the output of PWM<sub>X</sub>A or PWM<sub>X</sub>B to a high level.
- **Clear Low:** Clear the output of PWM<sub>X</sub>A or PWM<sub>X</sub>B by setting it to a low level.
- **Toggle:** Change the current output level of PWM<sub>X</sub>A or PWM<sub>X</sub>B to the opposite value. If it is currently pulled high, pull it low; or vice versa.

- Do Nothing: Keep both outputs PWM<sub>X</sub>A and PWM<sub>X</sub>B unchanged. In this state, interrupts can still be triggered.

The configuration of actions on outputs is done by using registers PWN_GEN<sub>X</sub>_A_REG and PWN_GEN<sub>X</sub>_B_REG. So, the action to be taken on each output is set independently. Also there is great flexibility in selecting actions to be taken on a given output based on events. More specifically, any event listed in Table 29.3-2 can operate on either output PWM<sub>X</sub>A or PWM<sub>X</sub>B. To check out registers for particular generator 0, 1 or 2, please refer to register description in Section 29.4.

---

### Waveforms for Common Configurations

Figure 29.3-14 presents the symmetric PWM waveform generated when the PWM timer is counting up and down. DC 0%–100% modulation can be calculated via the formula below:

\[ \text{Duty} = \left( \frac{\text{Period - A}}{\text{Period}} \right) \]

If A matches the PWM timer value and the PWM timer is incrementing, then the PWM output is pulled up. If A matches the PWM timer value while the PWM timer is decrementing, then the PWM output is pulled low.

---

**Footer:**
Espressif Systems
661 ESP32 TRM (Version 5.6)
Submit Documentation Feedback