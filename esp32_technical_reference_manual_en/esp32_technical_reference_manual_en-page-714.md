**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Section Header:**
Register 29.58. PWM_FAULT_DETECT_REG (0x00e4)

**Table Description:**
- The table lists various registers related to PWM events and their functions.
- Each row describes a specific register with its name, function description, access mode (R/W), bit positions in the register.

**Register Descriptions:**

1. **PWM_EVENT_F2**
   - Set and reset by hardware
   - If set, event_f2 is on-going

2. **PWM_EVENT_F1**
   - Set and reset by hardware
   - If set, event_f1 is on-going

3. **PWM_EVENT_F0**
   - Set and reset by hardware
   - If set, event_f0 is on-going

4. **PWM_F2_POLE**
   - Set event_f2 trigger polarity on FAULT2 source from GPIO matrix.
   - 0: level low; 1: level high (R/W)

5. **PWM_F1_POLE**
   - Set event_f1 trigger polarity on FAULT2 source from GPIO matrix
   - 0: level low, 1: level high

6. **PWM_F0_POLE**
   - Set event_f0 trigger polarity on FAULT2 source from GPIO matrix.
   - 0: level low; 1: level high (R/W)

7. **PWM_F2_EN**
   - Set to enable the generation of event_f2
   - Access mode is R/W

8. **PWM_F1_EN**
   - Set to enable the generation of event_f1.
   - Access mode is R/W

9. **PWM_F0_EN**
   - Set to enable the generation of event_f0 (R/W)

**Section Header:**
Register 29.59. PWM_CAP_TIMER_CFG_REG (0x00e8)

**Table Description:**
- The table lists various registers related to capture timer configuration.
- Each row describes a specific register with its name, function description, access mode.

10. **PWM_CAP_SYNC_SW**
    - Set this bit to force a capture timer sync; the capture timer is loaded with the value in the phase register (WO)

11. **PWM_CAP_SYNCI_SEL**
    - Capture module sync input selection.
    - 0: none
    - 1: timer0 sync_out, 2: timer1 sync_out, 3: timer2 sync_out, 4: SYNCO from GPIO matrix,
      5: SYNC1 from GPIO matrix, 6: SYNC2 from GPIO matrix (R/W)

12. **PWM_CAP_SYNCI_EN**
    - When set, the capture timer sync is enabled
    - Access mode is R/W

13. **PWM_CAP_TIMER_EN**
    - When set, the capture timer incrementing under APB_clk is enabled.
    - Access mode is (R/W)

**Footer:**
Espressif Systems  
Submit Documentation Feedback  
ESP32 TRM (Version 5.6)