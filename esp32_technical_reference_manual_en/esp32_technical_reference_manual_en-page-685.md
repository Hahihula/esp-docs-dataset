**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Section Header:**
GoBack

**Register Information for Register 29.11:**
- **Title:** PWM_TIMER2_CFG1_REG (0x0028)
- **Description of Fields in the Register:**
  - **PWM_TIMER2_MOD**: 
    - Description: PWM timer2 working mode.
    - Values:
      - `0`: freeze
      - `1`: increase mode, `2`: decrease mode,
      - `3`: up-down mode. (R/W)
  - **PWM_TIMER2_START**:
    - Description: PWM timer2 start and stop control.
    - Values:
      - `TEZ; 1`: if PWM timer2 starts, then stops at TEP
      - `2`: PWM timer2 starts and runs on;
      - `3`: PWM timer2 starts and stops at the next TEP. (R/W)
- **Register Address:** 
  - `0x0028`

**Register Information for Register 29.12:**
- **Title:** PWM_TIMER2_SYNC_REG (0x002c)
- **Description of Fields in the Register:**
  - **PWM_TIMER2_PHASE_DIR**:
    - Description: Phase for timer reload at sync event.
    - Values:
      - `0`: increase
      - `1`: decrease. (R/W)
  - **PWM_TIMER2_PHASE**:
    - Description: Phase for timer reload at sync event.
    - Values:
      - `0`: increase; `1`: decrease, `(R/W)`
  - **PWM_TIMER2_SYNCSEL**:
    - Description: PWM timer2 sync out selection.
    - Values:
      - `TEZ`
      - `TEP`
      - `other- wise`: sync_out is always O. (R/W)
  - **PWM_TIMER2_SYNC_SW**:
    - Description: Toggling this bit will trigger a software sync.
    - Access: `(R/W)`
  - **PWM_TIMER2_SYNCI_EN**:
    - Description: When set, timer reloading with phase on sync input event is enabled. (R/W)

**Footer Information:**
- Company Name: Espressif Systems
- Document Version and Link for Feedback: ESP32 TRM (Version 5.6) Submit Documentation Feedback

(Note: The binary representation of the registers' fields has been transcribed as it appears in the image, with spaces between bits.)