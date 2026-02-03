**Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Body Text:**
Rising edge (RED) and falling edge (FED) delays may be set up independently. The delay value is programmed using the 16-bit registers MCPWM_DTx_RED and MCPWM_DTx_FED. The register value represents the number of clock (DT_clk) periods by which a signal edge is delayed. DT_CLK can be selected from PWM_clk or PT_clk through register MCPWM_DTx_CLK_SEL.

To calculate the delay on falling edge (FED) and rising edge (RED), use the following formulas:

**Formulas:**
- FED = MCPWM_DTx_FED × T_Dt_clk
- RED = MCPWM_DTx_RED × T_Dt_clk

**Footer Information:**
Espressif Systems  
1355  
Submit Documentation Feedback  
ESP32-S3 TRM (Version 1.7)