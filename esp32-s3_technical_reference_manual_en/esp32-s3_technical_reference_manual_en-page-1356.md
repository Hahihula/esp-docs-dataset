**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Section Header:**
36.3.3.3 PWM Carrier Submodule

**Body Text:**
The coupling of PWM output to a motor driver may need isolation with a transformer. Transformers deliver only AC signals, while the duty cycle of a PWM signal may range anywhere from 0% to 100%. The PWM carrier submodule passes such a PWM signal through a transformer by using a high frequency carrier to modulate the signal.

**Subsection Title:**
Function Overview

**List (Key Characteristics):**
- Carrier frequency
- Pulse width of the first pulse
- Duty cycle of the second and the subsequent pulses
- Enabling/disabling the carrier function

**Subsection Title:**
Operational Highlights

**Body Text:**
The PWM carrier clock (PC_clk) is derived from PWMyclk. The frequency and duty cycle are configured by the MCPWM_CARRIERx PRESCALE and MCPWM_CARRIERx DUTY bits in the MCPWM_CARRIERx_CFG_REG register. The purpose of one-shot pulses is to provide high-energy impulse to reliably turn on the power switch. Subsequent pulses sustain the power-on status. The width of a one-shot pulse is configurable with the MCPWM_CARRIERx_OSHTWTH bits. Enabling/disabling of the carrier submodule is done with the MCPWM_CARRIERx_EN bit.

**Subsection Title:**
Waveform Examples

**Body Text:**
Figure 36.3-26 shows an example of waveforms, where a carrier is superimposed on original PWM pulses. This figure do not show the first one-shot pulse and the duty-cycle control. Related details are covered in the following two sections.

**Image Description (Caption):**
Figure 36.3-26. Example of Waveforms Showing PWM Carrier Action

**Footer:**
Espressif Systems
1356 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback