**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Back Link:**
GoBack

**Register Information for MCPWM_CAP_TIMER_CFG_REG (0x0E8):**

- **Field Description:** 
  - `MCPWM_CAP_TIMER_EN`
    - When set, capture timer incrementing under APB_clk is enabled. (R/W)
  - `MCPWM_CAP_SYNCI_EN`
    - When set, capture timer sync is enabled. (R/W)
  - `MCPWM_CAP_SYNCI_SEL`
    - Capture module sync input selection.
      - 0: none
      - 1: timer0 sync_out
      - 2: timer1 sync_out
      - 3: timer2 sync_out
      - 4: SYNCO from GPIO matrix
      - 5: SYNC1 from GPIO matrix
      - 6: SYNC2 from GPIO matrix (R/W)
  - `MCPWM_CAP_SYNC_SW`
    - When reg_cap_synci_en is 1, write 1 will trigger a capture timer sync.
      - Capture timer is loaded with value in phase register. (WT)

**Register Information for MCPWM_CAP_TIMER_PHASE_REG (0x0EC):**

- **Field Description:**
  - `MCPWM_CAP_TIMER_PHASE`
    - Phase value for capture timer sync operation.

**Footer:**
Espressif Systems
1401 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback