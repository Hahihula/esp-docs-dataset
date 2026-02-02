**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Section Heading: One-Shot Pulse**

**Body Text:**
The width of the first pulse is configurable. It may assume one of 16 possible values and is described by the formula below:

\[ T_{\text{1stpulse}} = T_{PWM\_M\_clk} \times 8 \times (PWM\_CARRIER \times PRESCALE + 1) \times (PWM\_CARRIER \times OSHTWTH + 1) \]

**Where:**
- \( T_{PWM\_clk} \) is the period of the PWM clock (PWM_clk).
- \( (PWM\_CARRIER \times OSHTWTH + 1) \) is the width of the first pulse whose value ranges from 1 to 16.
- \( (PWM\_CARRIER \times PRESCALE + 1) \) is the PWM carrier clock’s (PC_clk) prescaler value.

The first one-shot pulse and subsequent sustaining pulses are shown in Figure 29.3-27.

**Figure Caption:**
Figure 29.3-27. Example of the First Pulse and the Subsequent Sustaining Pulses of the PWM Carrier Sub-module

**Subsection Heading: Duty Cycle Control**

**Body Text:**
After issuing the first one-shot pulse, the remaining PWM signal is modulated according to the carrier frequency. Users can configure the duty cycle of this signal. Tuning of duty may be required, so that the signal passes through the isolating transformer and can still operate (turn on/off) the motor drive, changing rotation speed and direction.

The duty cycle may be set to one of seven values, using \( PWM\_CARRIER \times DUTY \), or bits [7:5] of register \( PWM\_CARRIER \times CFG\_REG \).

Below is the formula for calculating the duty cycle:

\[ Duty = \frac{PWM\_CARRIER \times DUTY}{8} \]

All seven settings of the duty cycle are shown in Figure 29.3-28.

**Footer:**
Espressif Systems
674 ESP32 TRM (Version 5.6)
Submit Documentation Feedback