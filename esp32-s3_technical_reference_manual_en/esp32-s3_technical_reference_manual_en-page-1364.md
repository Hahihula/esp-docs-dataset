**Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Subtitle:**
36.5 Registers

**Body Text:**
The addresses in this section are relative to Motor Control PWM0 and Motor Control PWM1 base address provided in Table 4.3-3 in Chapter 4 System and Memory.

**Table Descriptions with Labels:**

1. **Register 36.1. MCPWM_CLK_CFG_REG (0x0000)**
   - Description:
     - `MCPWM_CLK PRESCALE`
     - Period of PWM clk = 6.25ps * (PWM_CLK_PRESCALE + 1). (R/W)
   - Binary Representation: [Binary bits representation with reserved bits and reset value]

2. **Register 36.2. MCPWM_TIMERO_CFG0_REG (0x0004)**
   - Description:
     - `MCPWM_TIMERO PRESCALE`
     - Period of PTO_clk = Period of PWM_clk * (PWM_TIMERO_PRESCALE + 1). (R/W)
   - Binary Representation: [Binary bits representation with reserved bits and reset value]

3. **Register 36.2. MCPWM_TIMERO_PERIOD (0x0008)**
   - Description:
     - `Period shadow register of PWM timer0. (R/W)`
   - Binary Representation: [Binary bits representation with reserved bits and reset value]

4. **Register 36.2. MCPWM_TIMERO_PERIOD_UPMETHOD (0x000C)**
   - Description:
     - `Update method for active register of PWM timer0 period.
       O: immediate; 1: TEZ; 2: sync; 3: TEZ | sync. TEZ here and below means timer equal zero event.`
   - Binary Representation: [Binary bits representation with reserved bits]

**Footer Information:**
Espressif Systems
Page number: 1364
Document version: ESP32-S3 TRM (Version 1.7)
Link to Submit Documentation Feedback