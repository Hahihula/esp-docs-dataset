**Title:**
Chapter 13 Process ID Controller (PID)

**Diagram Description and Text in Diagrams:**

- **Level 2 interrupt occurs.**
  - PID = 4
    ```
    PIDCTRL_LEVEL_REG = XXXX X
    PIDCTRL_FROM_1_REG = XXXX X
    PIDCTRL_FROM_2_REG = XXXX X
    PIDCTRL_FROM_3_REG = XXXX X
    PIDCTRL_FROM_4_REG = XXXX X
    PIDCTRL_FROM_5_REG = XXXX X
    PIDCTRL_FROM_6_REG = XXXX X
    PIDCTRL_FROM_7_REG = XXXX X
    ```
  - No interrupt occurs.

- **Level 5 interrupt occurs.**
  - PID = 0
    ```
    PIDCTRL_LEVEL_REG = 2
    PIDCTRLFrom_1_REG = XXXX X
    PIDCTRLFrom_2_REG = 0000 100
    PIDCTRLFrom_3_REG = XXXX X
    PIDCTRLFrom_4_REG = XXXX X
    PIDCTRLFrom_5_REG = XXXX X
    PIDCTRLFrom_6_REG = XXXX X
    PIDCTRLFrom_7_REG = XXXX X
    ```
  - PID = 0

- **NMI interrupt occurs.**
  - PID = 0
    ```
    PIDCTRL_LEVEL_REG = 5
    PIDCTRLFrom_1_REG = XXXX X
    PIDCTRLFrom_2_REG = 0000 100
    PIDCTRLFrom_3_REG = XXXX X
    PIDCTRLFrom_4_REG = XXXX X
    PIDCTRLFrom_5_REG = 0010 000
    PIDCTRLFrom_6_REG = XXXX X
    PIDCTRLFrom_7_REG = 0101 000
    ```
  - PID = 0

**Figure Caption:**
Figure 13.3-1. Interrupt Nesting

**Body Text Explanation of Diagrams and Process Flow:**

If the system is currently in a nested interrupt and needs to revert to the previous interrupt, register `PIDCTRL_LEVEL_REG` must be restored based on the information recorded in register `PIDCTRL_FROM_n_REG` in step 5.

In step 6, after the values of register `PIDCTRL_PID_CONFIRM_REG` and register `PIDCTRL_NMI_MASK_DISABLE_REG` are set to 1, PID Controller will not immediately switch PID to the value of register `PIDCTRL_PID_NEW_REG`, nor disable CPU NMI Interrupt Mask signal at once. Instead, PID Controller performs each task after a different number of clock cycles. The numbers of clock cycles are the values

**Footer:**
Espressif Systems
274 Submit Documentation Feedback ESP32 TRM (Version 5.6)