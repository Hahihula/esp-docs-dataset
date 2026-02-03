**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Section Heading: One-Shot Pulse**

**Body Text:**
The width of the first pulse is configurable. It may assume one of 16 possible values and is described by the formula below:

\[ T_{\text{1stpulse}} = \frac{T_{PWM\_clk} \times 8}{(\text{MCPWM\_CARRIER}_x \cdot \text{PRESCALE} + 1) \times (\text{MCPWM\_CARRIER}_x \cdot \text{OSHTWTH} + 1)} \]

**Where:**
- \( T_{PWM\_clk} \) is the period of the PWM clock (PWM_clk).
- \( (\text{MCPWM\_CARRIER}_x \cdot \text{OSHTWTH} + 1) \) is the width of the first pulse whose value ranges from 1 to 16.
- \( (\text{MCPWM\_CARRIER}_x \cdot \text{PRESCALE} + 1) \) is the PWM carrier clock's (PC_clk) prescaler value.

The first one-shot pulse and subsequent sustaining pulses are shown in Figure 36.3-27.

**Figure Caption:**
Figure 36.3-27. Example of the First Pulse and the Subsequent Sustaining Pulses of the PWM Carrier Sub-module

**Subsection Heading: Duty Cycle Control**

**Body Text:**
After issuing the first one-shot pulse, the remaining PWM signal is modulated according to the carrier frequency. Users can configure the duty cycle of this signal. Tuning of duty may be required so that the signal passes through the isolating transformer and can still operate (turn on/off) the motor drive, changing rotation speed and direction.

The duty cycle may be set to one of seven values using \( \text{MCPWM\_CARRIER}_x \cdot \text{DUTY} \), or bits [7:5] of register \( \text{MCPWM\_CARRIER}_x \cdot \text{CFG\_REG} \).

Below is the formula for calculating the duty cycle:

\[ \text{Duty} = \frac{\text{MCPWM\_CARRIER}_x \cdot \text{DUTY}}{8} \]

**Footer:**
Espressif Systems
1357 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback