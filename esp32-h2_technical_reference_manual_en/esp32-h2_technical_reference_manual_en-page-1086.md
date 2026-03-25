

```markdown
## 36.3.3.3 PWM Carrier Module

The coupling of PWM output to a motor driver may need isolation with a transformer. Transformers deliver only AC signals, while the duty cycle of a PWM signal may range anywhere from 0% to 100%. The PWM carrier module passes such a PWM signal through a transformer by using a high-frequency carrier to modulate the signal.

### Function Overview

The following key characteristics of this module are configurable:

*   Carrier frequency
*   Pulse width of the first pulse
*   Duty cycle of the second and the subsequent pulses
*   Enabling/disabling the carrier function

### Operational Highlights

The PWM carrier clock (PC_CLK) is derived from PWM_CLK. The frequency and duty cycle are configured by the `MCPWM_CARRIERx_PRESCALE` and `MCPWM_CARRIERx_DUTY` bits in the `MCPWM_CARRIERx_CFG_REG` register. The purpose of one-shot pulses is to provide high-energy impulse to reliably turn on the power switch. Subsequent pulses sustain the power-on status. The width of a one-shot pulse is configurable with the `MCPWM_CARRIERx_OSHTWTH` field. Enabling/disabling of the carrier module is done with the `MCPWM_CARRIERx_EN` bit.

### Waveform Examples

Figure 36.3-28 shows an example of waveforms, where a carrier is superimposed on original PWM pulses. This figure does not show the first one-shot pulse and the duty-cycle control. Related details are covered in the following two sections.
```