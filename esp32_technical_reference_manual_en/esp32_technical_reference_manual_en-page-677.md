**Chapter Title:**
Motor Control PWM (MCPWM)

**Subsections and Descriptions with Code Examples**

- **29.3.4.2 Capture Timer**
  - The capture timer is a 32-bit counter incrementing continuously, once enabled.
  - On the input it has an APB clock running typically at 80 MHz.

- **29.3.4.3 Capture Channel**
  - When a capture signal coming to a capture channel will be inverted first if needed and then prescaled; finally specified edges of preprocessed capture signals trigger events.
  - The edge that triggers the event is recorded in register PWM_CAPx_EDGE, where x can range from 1 to 256.

**Section Title:**
Register Summary

- **Description:** 
  - Addresses given are relative to the MCPWM base address provided. See Table 3.3-6 for details.
  
- **Table of Register Abbreviations and Access Types**

| Name                          | Description                                                                                   | PWM0       | PWM1      | Acc |
|-------------------------------|---------------------------------------------------------------------------------------------|------------|-----------|-----|
| Prescaler configuration        | Configuration of the prescaler                                                                | 0x3FF5E000 | 0x3FF6C000 | R/W |
| PWM_CLK_CFG_REG               |                                                                                               |            |           |     |
| PWM_Timer_0_Configuration_and_Status | Timer period and update method                   | 0x3FF5E004 | 0x3FF6C004 | R/W |
| PWM_TIMER0_CFG0_REG           | Working mode and start/stop control                                                          | 0x3FF5E008 | 0x3FF6C008 | R/W |
| PWM_TIMER0_SYNC_REG          | Synchronization settings                                                                      | 0x3FF5E00C | 0x3FF6C00C | R/W |
| PWM_TIMER0_STATUS_REG        | Timer status                                                                                 | 0x3FF5E010 | 0x3FF6C010 | RO  |
| PWM_Timer_1_Configuration_and_Status | Timer update method and period                   | 0x3FF5E014 | 0x3FF6C014 | R/W |
| PWM_TIMER1_CFG0_REG           | Working mode and start/stop control                                                          | 0x3FF5E018 | 0x3FF6C018 | R/W |
| PWM_TIMER1_SYNC_REG          | Synchronization settings                                                                      | 0x3FF5E01C | 0x3FF6C01C | R/W |
| PWM_TIMER1_STATUS_REG        | Timer status                                                                                 | 0x3FF5E020 | 0x3FF6C020 | RO  |
| PWM_Timer_2_Configuration_and_Status | Timer update method and period                   | 0x3FF5E024 | 0x3FF6C024 | R/W |
| PWM_TIMER2_CFG0_REG           | Working mode and start/stop control                                                          | 0x3FF5E028 | 0x3FF6C028 | R/W |
| PWM_TIMER2_SYNC_REG          | Synchronization settings                                                                      | 0x3FF5E02C | 0x3FF6C02C | R/W |
| PWM_TIMER2_STATUS_REG        | Timer status                                                                                 | 0x3FF5E030 | 0x3FF6C030 | RO  |

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback