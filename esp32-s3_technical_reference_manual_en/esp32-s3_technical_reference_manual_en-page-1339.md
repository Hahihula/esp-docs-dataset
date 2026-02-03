**Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Diagram Description and Labels in Image:**

- **Figure Caption:** Figure 36.3-13. Submodules Inside the PWM Operator

- Diagram Components:
  - A -> PWMA
  - B -> PWMB
  - PWMA -> Dead Time Generator
    - Dead Time Generator -> PWMB
  - PWMA -> PWM Carrier
    - PWM Carrier -> PWMB
  - PWMA -> Fault Handler
    - Fault Handler -> PWMB
  - PWMB -> PWMxA, PWMxB

- Additional Labels:
  - timer value (arrow pointing to PWMA)
  - timer status (arrow going from PWMB)

**Fault Events:**
- fault event 0 
- fault event 1 
- fault event 2 

**Footer Information:**
- Espressif Systems
- Page Number: 1339
- Document Title: ESP32-S3 TRM (Version 1.7)
- Link Texts:
  - Submit Documentation Feedback