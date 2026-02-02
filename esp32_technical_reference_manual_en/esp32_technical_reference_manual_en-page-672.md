**Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Figure Captions and Descriptions:**

- **Figure 29.3-24:** Active High (AH) Dead Time Waveforms

  - Diagram showing the waveform for an active high dead time with labels:
    - PWMAxA Input
    - DTRED
    - DTFED
    - PWMBxA Output

- **Figure 29.3-25:** Active Low (AL) Dead Time Waveforms

  - Diagram showing the waveform for an active low dead time with labels:
    - PWMAxA Input
    - DTRED
    - DTFED
    - PWMBxA Output

**Body Text:**

Rising edge (RED) and falling edge (FED) delays may be set up independently. The delay value is programmed using the 16-bit registers PWM_DTx_RED and PWM_DTx_FED. The register value represents the number of clock (DT_clk) periods by which a signal edge is delayed. DT_CLK can be selected from PWM_clk or PT_clk through register PWM_DTx_CLK_SEL.

To calculate the delay on falling edge (FED) and rising edge (RED), use the following formulas:

\[ FED = PWM_DTx_FED \times T_{DT_clk} \]
\[ RED = PWM_DTx_RED \times T_{DT_clk} \]

**Subsection Title:**
29.3.3.3 PWM Carrier Submodule

**Body Text:**

The coupling of PWM output to a motor driver may need isolation with a transformer. Transformers deliver only AC signals, while the duty cycle of a PWM signal may range anywhere from 0% to 100%. The PWM carrier frequency is typically in the audio band (20 Hz - 20 kHz).

**Footer:**
Espressif Systems
672 ESP32 TRM (Version 5.6)
Submit Documentation Feedback