**Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Header:**
Register 29.33. PWM_GEN1_CFGO_REG (0x008Q)

**Diagram Description:**
- The diagram shows a bit map with labels for each bit position from the most significant to least significant.
- Labels include "PWM_GEN1_T1_SEL", "PWM_GEN1_TO_SEL", and others, indicating different configuration settings.

**Body Text:**

- **PWM_GEN1_T1_SEL**: Source selection for PWM generator 1 event_t1; taking effect immediately. O: fault_event0, 1: fault_event1, 2: fault_event2, 3: sync_taken, 4: none.
- **PWM_GEN1_TO_SEL**: Source selection for PWM generator 1 event_t0; taking effect immediately. O: fault_event0, 1: fault_event1, 2: fault_event2, 3: sync_taken, 4: none.

- **PWM_GEN1_CFG_UPMETHOD**: Updating method for PWM generator 1’s active register of configuration.
  - Immediate update (O): when bit0 is set to 1
  - TEZ mode; when bit1 is set to 1
  - TEP mode, when bit2 is set to 1
  - Sync. bit3: disable the update.

**Footer Information:**
- Page number and document version:
  - "697 ESP32 TRM (Version 5.6)"
- Company name at bottom left corner.
- Link for submitting documentation feedback on the right side of footer section.