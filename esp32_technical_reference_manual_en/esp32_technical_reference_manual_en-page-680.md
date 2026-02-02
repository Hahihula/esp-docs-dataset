**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Table of Registers and Descriptions**

| Name                          | Description                                    | PWO   | PWM1    | Acc |
|-------------------------------|-----------------------------------------------|-------|---------|-----|
| Enable update of active registers | -PWM_UPDATE_CFG_REG | Enable update | 0x3FF5E10C | R/W |
| Manage Interrupts            | -INT_ENA_PWM_REG, -INT_RAW_PWM_REG, -INT_ST_PWM_REG, -INT_CLR_PWM_REG | Interrupt enable bits, Raw interrupt status, Masked interrupt status, Interrupt clear bits | 0x3FF5E114 (R/W), 0x3FF6C114 (RO), 0x3FF5E118 (RO), 0x3FF6C11C (WO) |

**Section Title:**
29.5 Registers

**Body Text:**
The addresses in this section are relative to the MCPWM base address provided in Table 3.3-6 in Chapter 3 System and Memory. The absolute register addresses are listed in Section **29.4 Register Summary**.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

**Register Descriptions:**

1. **Register 29.1. PWM_CLK_CFG_REG (0x0000)**
   - Description:
     - `PWM_CLK_PRESCALE`: Period of PWM_clk = 6.25ns * (PWM_CLK_PRESCALE + 1). (R/W)
   - Binary Representation: 
     ```
     31  0
     8    7    0
     0  O  O  O  O  O  O  O  O  O  R  E  S  T
     ```

2. **Register 29.2. PWM_TIMERO_CFGO_REG (0x0004)**
   - Description:
     - `PWM_TIMERO_PERIOD_UPMETHOD`: Updating method for active register of PWM timer0 period.
       - O: immediately,
       - 1: update at TEZ
       - 2: update at sync
       - 3: update at TEZ or sync. TEZ here and below means that the event happens when the timer equals to zero (R/W)
     - `PWM_TIMERO_PERIOD`: Period shadow register of PWM timer0.
     - `PWM_TIMERO_PRESCALe`: Period of PTO_clk = Period of PWM_clk * (PWM_TIMERO_PRESCALe + 1). (R/W)

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32 TRM (Version 5.6)