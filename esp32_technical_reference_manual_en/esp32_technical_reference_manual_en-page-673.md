**Title:**
Chapter 29 Motor Control PWM (MCPWM)

**GoBack**

**Body Text:**
submodule passes such a PWM signal through a transformer by using a high frequency carrier to modulate the signal.

**Subheading: Function Overview**

The following key characteristics of this submodule are configurable:
- Carrier frequency
- Pulse width of the first pulse
- Duty cycle of the second and the subsequent pulses
- Enabling/disabling the carrier function

**Subheading: Operational Highlights**

The PWM carrier clock (PC_clk) is derived from PWMyclk. The frequency and duty cycle are configured by the PWM_CARRIERx PRESCALE and PWM_CARRIERx DUTY bits in the PWM_CARRIERx_CFG_REG register.
The purpose of one-shot pulses is to provide high-energy impulse to reliably turn on the power switch. Subsequent pulses sustain the power-on status. The width of a one-shot pulse is configurable with the PWM_CARRIERx_OSHTWTH bits. Enabling/disabling of the carrier submodule is done with the PWM_CARRIERx_EN bit.

**Subheading: Waveform Examples**

Figure 29.3-26 shows an example of waveforms, where a carrier is superimposed on original PWM pulses.
This figure do not show the first one-shot pulse and the duty-cycle control. Related details are covered in the following two sections.

**Image Description (Waveform Example):**
The image depicts examples of waveforms showing PWM Carrier Action with labels for "PWMxA", "PWMxB", and a section labeled as "Carrier". The diagram is divided into three main areas, each representing different signal states or phases. 

**Footer:**
Espressif Systems
673 ESP32 TRM (Version 5.6)
Submit Documentation Feedback