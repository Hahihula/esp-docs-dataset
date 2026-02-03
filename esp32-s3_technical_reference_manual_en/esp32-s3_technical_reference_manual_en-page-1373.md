**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**GoBack Link:** GoBack

**Section Header:**
Register 36.14. MCPWM_TIMER_SYNCI_CFG_REG (0x0034)

**Continuation Note:**
Continued from the previous page.

**Subsection Title and Description:**
MCPWM_TIMER2_SYNCISCEL
Select sync input for PWM timer2.
(R/W)
- **List of options with corresponding numbers:** 
  - 1: PWM timer0 sync_out;
  - 2: PWM timer1 sync_out;
  - 3: PWM timer2 sync_out;
  - 4: SYNCO from GPIO matrix;
  - 5: SYNC1 from GPIO matrix;
  - 6: SYNC2 from GPIO matrix
- **Other values:** no sync input selected.

**Subsection Title and Description:**
MCPWM_EXTERNAL_SYNCIO_INVERT
Invert SYNCO from GPIO matrix.
(R/W)

**Subsection Title and Description:**
MCPWM_EXTERNAL_SYNCI1_INVERT
Invert SYNC1 from GPIO matrix. (R/W)

**Subsection Title and Description:**
MCPWM_EXTERNAL_SYNCI2_INVERT
Invert SYNC2 from GPIO matrix.

**Section Header:**
Register 36.15. MCPWM_OPERATOR_TIMERSCEL_REG (0x0038)

**Binary Representation Diagram:** 
- A binary representation of a register with bits labeled as follows:
  - Bit positions are numbered, and the diagram shows that all bit values except for one specific position is set to '0'.
  
**Subsection Title:**
MCPWM_OPERATOR0_TIMERSCEL
Select which PWM timer’s is the timing reference for PWM operator0.
(R/W)
- **Options:** 
  - 0: timer0; 1: timer1; 2: timer2.

**Subsection Title:**
MCPWM_OPERATOR1_TIMERSCEL
Select which PWM timer's is the timing reference for PWM operator1. (R/W)
- **Options:** 
  - 0: timer0; 1: timer1; 2: timer2.

**Subsection Title:**
MCPWM_OPERATOR2_TIMERSCEL
Select which PWM timer’s is the timing reference for PWM operator2.
(R/W)
- **Options:** 
  - 0: timer0; 1: timer1; 2: timer2. 

**Footer Information:**
Espressif Systems, ESP32-S3 TRM (Version 1.7), Submit Documentation Feedback