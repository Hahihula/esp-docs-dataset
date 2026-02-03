**Chapter Title:**
Motor Control PWM (MCPWM)

**Section Header:**
Priority level

**Table:**
| Priority level | Event |
|-----------------|-------|
| 4               | DT1   |
| 5               | DTEB  |
| 6               | DTEA  |
| 7 (lowest)     | DTEP  |

**Notes Section:**

1. UTEP and UTEZ do not happen simultaneously. When the PWM timer is in count-up mode, UTEP will always happen one cycle earlier than UTEZ, as demonstrated in Figure 36.3-10, so their action on PWM signals will not interrupt each other. When the PWM timer is in count-up-down mode, UTEP will not occur.
2. DTEP and DTEZ do not happen simultaneously. When the PWM timer is in count-down mode, DTEZ will always happen one cycle earlier than DTEP, as demonstrated in Figure 36.3-11, so their action on PWM signals will not interrupt each other. When the PWM timer is in count-up-down mode, DTEZ will not occur.

**PWM Signal Generation Section:**

The PWM generator submodule controls the behavior of outputs PWMxA and PWMxB when a particular timing event occurs. The timing events are further qualified by the PWM timer’s counting direction (up or down). Knowing the counting direction, the submodule may then perform an independent action at each stage of the PWM timer counting up or down.

**Instructions for Configuring Actions:**

The following actions may be configured on outputs PWMxA and PWMxB:

- **Set High:** Set the output of PWMxA or PWMxB to a high level.
- **Clear Low:** Clear the output of PWMxA or PWMxB by setting it to a low level.
- **Toggle:** Change the current output level of PWMxA or PWMxB to the opposite value. If it is currently pulled high, pull it low; vice versa.

**Additional Instructions:**

- Do Nothing:
  - Keep both outputs PWMxA and PWMxB unchanged. In this state, interrupts can still be triggered.
  
The configuration of actions on outputs is done by using registers MCPWN_GENx_A_REG and MCPWN_GENx_B_REG. So the action to be taken on each output is set independently.

**Waveforms for Common Configurations:**

Figure 36.3-14 presents the symmetric PWM waveform generated when the PWM timer is counting up and down. DC 0%-100% modulation can be calculated via the formula below:

\[ \text{Duty} = \left( \frac{\text{Period - A}}{\text{Period}} \right) \times 100\% \]

**Footer:**
Espressif Systems
Page number: 1342
Document version: ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback