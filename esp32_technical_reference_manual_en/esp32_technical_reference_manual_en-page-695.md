**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**GoBack Link:** GoBack

---

**Section Header:**
Register 29.28. PWM_FHO_CFG1_REG (0x006c)

**Binary Register Diagram Description:**
- The diagram shows a binary register with bits labeled from left to right as follows:
  - 3
  - reserved
  - ...
  - 4
  - 5

**Register Description and Values:**  
PWM_FHO FORCE OST (R/W)  
A toggle triggers the software negation of this bit's value, which in turn triggers a one-shot mode action.  

- **Binary Value Representation:**
  ```
  0 1 0 0 0 0 0 0
  ```

**Register Description and Values:**  
PWM_FHO FORCE CBC (R/W)  
A toggle activates cycle-by-cycle mode actions.

- **Binary Value Representation:**
  ```
  0 1 0 0 0 0 0 0
  ```

**Register Description and Values:**  
PWM_FHO CBCPULSE  
The bit controls the refresh moment selection for a cycle-by-cycle action. When set to `1`, it triggers TFP (R/W).

- **Binary Value Representation:**
  ```
  0 1 0 0 0 0 0
  ```

**Register Description and Values:**  
PWM_FHO CLR OST (R/W)  
A toggle clears the on-going one-shot mode action.

- **Binary Value Representation:**
  ```
  0 1 0 0 0 0 0 
  ```

---

**Section Header:**
Register 29.29. PWM_FHO_STATUS_REG (0x0070)

**Binary Register Diagram Description:**  
Similar to the previous register, with bits labeled from left to right as follows:
- reserved
- ...
- 31

**Register Description and Values:**  
PWM_FHO OST ON (RO)  
Set by hardware. If set `1`, a one-shot mode action is on-going.

- **Binary Value Representation:**
  ```
  0 1 0 0 0 0 0
  ```

**Register Description and Values:**  
PWM_FHO CBC ON (RO)  
Set by hardware to indicate that the cycle-by-cycle mode actions are ongoing. 

---

**Footer Information:**
Espressif Systems  
Page Number: 695  
ESP32 TRM (Version 5.6)

**Link for Feedback Submission:**
Submit Documentation Feedback