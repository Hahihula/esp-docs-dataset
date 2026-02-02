**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**GoBack Link:** GoBack

---

**Section Header:**
Register 29.5. PWM_TIMERO_STATUS_REG (0x0010)

**Diagram Description for Register 29.5:**
- **PWM_TIMERO_DIRECTION**: Current direction of the PWM timer0 counter.
  - Values:
    - 31 to 17, bits are set as shown in binary format
    - Bit positions and values (from rightmost bit):
      - Reset value is all zeros

**Field Description for Register 29.5:**
- **PWM_TIMERO_DIRECTION**: Current direction of the PWM timer0 counter.
  - Values:
    - 0: increment, 1: decrement.

- **PWM_TIMERO_VALUE**: Current value of the PWM timer0 counter (Read Only).

---

**Section Header:**
Register 29.6. PWM_TIMER1_CFGO_REG (0x0014)

**Diagram Description for Register 29.6:**
- Similar to register 29.5, but with different bit positions and values.

**Field Description for Register 29.6:**

- **PWM_TIMER1_UP_METHOD**: Updating method for the active register of PWM timer1 period.
  - Values:
    - Reset value is all zeros

- **PWM_TIMER1_PERIOD**: Period shadow register of the PWM timer1 (Read/Write).

- **PWM_TIMER1_PRESCALE**: Period of PT1_clk = Period of PWM_clk * (PWM_TIMER1_PRESCALE + 1) (Read/Write)

---

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback