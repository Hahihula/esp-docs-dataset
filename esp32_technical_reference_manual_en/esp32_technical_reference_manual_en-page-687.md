**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**GoBack Link:** GoBack

---

**Section Header:**
Register 29.15. PWM_OPERATOR_TIMERSEL_REG (0x0038)

**Binary Representation of Register:**
```
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
```

**Description and Values for Each Bit Field in the Register:**

- **PWM_OPERATOR2_TIMERSEL:** 
  - Description: Select the PWM timer for PWM operator2’s timing reference.
  - Options:
    - `0`: timer0, 1: timer1, 2: timer2. (R/W)

- **PWM_OPERATOR1_TIMERSEL:** 
  - Description: Select the PWM timer for PWM operator1’s timing reference.
  - Options:
    - `0`: timer0, 1: timer1, 2: timer2. (R/W)

- **PWM OPERATOR0_TIMERSEL:** 
  - Description: Select the PWM timer for PWM operator0's timing reference.
  - Options:
    - `0`: timer0, 1: timer1, 2: timer2. (R/W)

---

**Section Header:**
Register 29.16. PWM_GENO_STMP_CFG_REG (0x003c)

**Binary Representation of Register:**
```
0 0 0 0 0 0 0 0 0 0 0 0
```

**Description and Values for Each Bit Field in the Register:**

- **PWM_GENO_B_SHOW_FULL:** 
  - Description: Set and reset by hardware. If set, PWM generator O time stamp B’s shadow register.ister is filled and to be transferred to time stamp B's active register.
  - Options:
    - `0`: cleared
    - `1`: updated with Shadow register latest value.

- **PWM_GENO_A_SHOW_FULL:** 
  - Description: Set and reset by hardware. If set, PWM generator A time stamp shadow register.ister is filled and to be transferred to time stamp A's active register.
  - Options:
    - `0`: cleared
    - `1`: updated with Shadow register latest value.

- **PWM_GENO_B_UPMETHOD:** 
  - Description: Updating method for PWM generator O time stamp B’s active register. When all bits are set to 0, immediately; when bit0 is set to 1: TEZ; when bit1 is set to 1: TEP; when bit2 is set to 1: sync; when bit3 is set to 1: disable the update.
  - Options:
    - `R/W`

- **PWM_GENO_A_UPMETHOD:** 
  - Description: Updating method for PWM generator O time stamp A’s active register. When all bits are set to Q, immediately; when bit0 is set to 1: TEZ; when bit1 is set to 1: TEP; when bit2 is set to 1: sync; when bit3 is set to 1: disable the update.
  - Options:
    - `R/W`

---

**Footer Information:** 
Espressif Systems
Page Number: 687
Document Title: ESP32 TRM (Version 5.6)
Link Texts: Submit Documentation Feedback