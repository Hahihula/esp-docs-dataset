**Title: Chapter 36 Motor Control PWM (MCPWM)**

**Subtitle: Register 36.56. MCPWM_FH2_CFGO_REG (0x0CDB8)**

**Table Description:**  
The table lists various registers related to the MCPWM module, each with a specific function and bit positions.

- **MCPWM_FH2_SW_CBC**: Enable register for software force cycle-by-cycle mode action. 0: disable, 1: enable.
- **MCPWM_FH2_F2_CBC**: event_f2 will trigger cycle-by-cycle mode action. 0: disable, 1: enable.
- **MCPWM_FH2_E1_CBC**: event_f1 will trigger cycle-by-cycle mode action. 0: disable, 1: enable.
- **MCPWM_FH2_F0_CBC**: event_f0 will trigger cycle-by-cycle mode action. 0: disable, 1: enable.
- **MCPWM_FH2_SW_OST**: Enable register for software force one-shot mode action. 0: disable, 1: enable.
- **MCPWM_FH2_F2_OST**: event_f2 will trigger one-shot mode action. 0: disable, 1: enable.
- **MCPWM_FH2_F1_OST**: event_f1 will trigger one-shot mode action. 0: disable, 1: enable.
- **MCPWM_FH2_FO_OST**: event_f0 will trigger one-shot mode action. 0: disable, 1: enable.

**Additional Registers and Their Functions:**  
- **MCPWM_FH2_A_CBC_D**: Cycle-by-cycle mode action on PWM2A when fault event occurs and timer is decreasing.
- **MCPWM_FH2_A_CBC_U**: Cycle-by-cycle mode action on PWM2A when fault event occurs and timer is increasing.

**One-shot Mode Actions:**  
- Various registers for one-shot actions with different configurations (e.g., force low, high; toggle).

**Footer:**
- "Espressif Systems"
- Page number 1399
- Document version ESP32-S3 TRM (Version 1.7)
- Link to submit documentation feedback