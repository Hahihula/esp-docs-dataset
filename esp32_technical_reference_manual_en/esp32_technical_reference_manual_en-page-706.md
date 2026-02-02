**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Back Link:**
GoBack

**Register Information:**
- **Register Name:** PWM_GEN2_CFG0_REG (0x00b8)
- **Address:** Not specified in the text.

**Binary Diagram Description:**
A binary diagram is shown with labels for each bit position from 31 to 0. The bits are labeled as follows:
- 31
- ... (bits not individually numbered, but implied continuation of a standard binary representation)

**Text Descriptions and Values under Binary Diagram:**
```
0   0   0   0   0   0   0   0   0   0   0   0   0   0
```

**Field Definitions with Values (Hexadecimal):**
- **PWM_GEN2_T1_SEL:** Source selection for PWM generator2 event_t1, take effect immediately. O: fault_event0; I: fault_event1; S: fault_event2; T: sync_taken; N: none.
  - (R/W)
  
- **PWM_GEN2_TO_SEL:** Source selection for PWM generator2 event_t0, take effect immediately. O: fault_event0; I: fault_event1; S: fault_event2; T: sync_taken; N: none.

- **PWM_GEN2_CFG_UPMETHOD:** Updating method for PWM generator2's active register of configuration.
  - R: immediately
  - When bit0 is set to:
    - TEZ (When bit1 is set)
    - TEP

**Footer Information:**
- Page Number: 706
- Document Title: ESP32 TRM (Version 5.6)

**Company and Feedback Link:**
Espressif Systems  
Submit Documentation Feedback