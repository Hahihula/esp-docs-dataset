**Title: Chapter 29 Motor Control PWM (MCPWM)**

---

### Register Description:

- **Register 29.53: PWM_DT2_RED_CFG_REG (0x0d0)**
  - **Description:** Shadow register for RED.
  - **Access Type:** Read/Write
  - **Bits Layout:**
    ```
    +-------------+-------------+
    |   16       |     15      |
    +-------------+-------------+
    | PWM_DT2_RED|             |
    +-------------+-------------+
    ```

- **Register 29.54: PWM_CARRIER2_CFG_REG (0x0d4)**
  - **Description:** Configuration register for Carrier 2.
  - **Access Type:** Read/Write
  - **Bits Layout with Descriptions:**
    ```
    +-------------+-------------+-------------+-------------+
    |   16       |     15      |    14       |     13      |
    +-------------+-------------+-------------+-------------+
    | PWM_CARRIER2_INVERT|PWM_CARRIER2_DUTY|PWM_CARRIER2_RESCALE|PWM_CARRIER2_EN|
    +-------------+-------------+-------------+-------------+
    ```

- **Bits Details:**
  - **PWM_CARRIER2_INVERT:** When set, invert the input of PWM2A and PWM2B for this submodule.
  - **PWM_CARRIER2_DUTY:** Carrier duty selection. Duty = PWM_CARRIER2_DUTY / 8 (R/W).
  - **PWM_CARRIER2_PRESCALE:** PWM carrier2 clock (PC_clk) prescale value. Period of PC_clk = period of PWM_CLK * (PWM_CARRIER2_PRESCALE + 1). (R/W)
  - **PWM_CARRIER2_EN:** When set, carrier2 function is enabled. When cleared, carrier2 is bypassed.
  
---

**Footer:**
- Espressif Systems
- ESP32 TRM (Version 5.6)