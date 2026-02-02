**Chapter Title:**
Chapter 13 Process ID Controller (PID)

**Section Heading and Description:**
- **Subsection:** PIDCTRL_INTERRUPT_ENABLE_REG determines whether the PID Controller identifies and registers an interrupt of certain priority. When a bit of register PIDCTRL_INTERRUPT_ENABLE_REG is 1, PID Controller will take action when CPU fetches instruction from the interrupt vector entry address of corresponding interrupt.
  
**Table Title (with description):**
- **Table Name:** Table 13.3-1. Interrupt Vector Entry Address
- The table lists priority levels and their associated interrupt vectors.

| Priority level | PIDCTRL_INTERRUPT_ENABLE_REG bit controlling interrupt identification | Interrupt vector entry address |
|-----------------|----------------------------------------------------------------------------------|--------------------------------|
| Level 1         | 1                                                                                   | PIDCTRL_INTERRUPT_ADDR_1_REG   |
| Level 2         | 2                                                                                   | PIDCTRL_INTERRUPT_ADDR_2_REG    |
| Level 3         | 3                                                                                   | PIDCTRL_INTERRUPT_ADDR_3_REG    |
| Level 4         | 4                                                                                   | PIDCTRL_INTERRUPT_ADDR_4_REG    |
| Level 5         | 5                                                                                   | PIDCTRL_INTERRUPT_ADDR_5_REG    |
| Level 6 (Debug) | 6                                                                                   | PIDCTRL_INTERRUPT_ADDR_6_REG    |
| NMI             | 7                                                                                   | PIDCTRL_INTERRUPT_ADDR_7_REG    |

**Subsection Heading and Description:**
- **Section:** Information Recording
- When PID Controller identifies an interrupt, it records three items of information in addition to switching PID to O. The recorded information includes the priority level of current interrupt, previous interrupt status of the system and the previous process running on the CPU.

**Additional Table Title (with description):**
- **Table Name:** Table 13.3-2. Configuration of PIDCTRL_LEVEL_REG
- This table records the priority levels in register PIDCTRL_LEVEL_REG.
  
| Value | Priority level of the current interrupt |
|-------|------------------------------------------|
| 0     | No interrupt                             |
| 1     | Level 1                                  |
| 2     | Level 2                                  |
| 3     | Level 3                                  |
| 4     | Level 4                                  |
| 5     | Level 5                                  |
| 6     | Level 6                                  |
| NMI   |                                          |

**Additional Information:**
- PID Controller also records in register PIDCTRL_FROM_n_REG the status of the system before the interrupt occurred. The bit width of register PIDCTRL_FROM_n_REG is 7.
  
**Footer Note:** 
Espressif Systems
Submit Documentation Feedback

**Document Footer (with version information):**
ESP32 TRM (Version 5.6)