

```markdown
Chapter 36 Motor Control PWM (MCPWM)

One-Shot Pulse

The width of the first pulse can be configured to 16 different values, which can be calculated by the following equation:

T₁stpulse = T_PWM_CLK × 8 × (MCPWM_CARRIERx_PRESCALE + 1) × (MCPWM_CARRIERx_OSHTWTH + 1)

Where:
*   T_PWM_CLK is the period of the PWM clock (PWM_CLK).
*   (MCPWM_CARRIERx_OSHTWTH + 1) is the width of the first pulse (whose value ranges from 1 to 16).
*   (MCPWM_CARRIERx_PRESCALE + 1) is the PWM carrier clock’s (PC_CLK) prescaler value.

The first one-shot pulse and subsequent sustaining pulses are shown in Figure 36.3-29.

Figure 36.3-29. Example of the First Pulse and the Subsequent Sustaining Pulses of the PWM Carrier Sub-module

Duty Cycle Control

After issuing the first one-shot pulse, the remaining PWM pulses are modulated according to the carrier frequency. Users can configure the duty cycle of this signal. Tuning of duty may be required, so that the signal passes through the isolating transformer and can still operate (turn on/off) the motor drive, changing rotation speed and direction.

The duty cycle may be set to one of seven values, using MCPWM_CARRIERx_DUTY, or bits [7:5] of register MCPWM_CARRIERx_CFG_REG.

Below is the formula for calculating the duty cycle:

Duty = MCPWM_CARRIERx_DUTY ÷ 8
```