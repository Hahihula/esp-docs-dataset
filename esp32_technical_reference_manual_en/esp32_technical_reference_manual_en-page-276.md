**Chapter Title:**
Chapter 13 Process ID Controller (PID)

**GoBack Link:** GoBack

---

**Section Header and Register Information with Binary Representation:**

- **Register Name**: PIDCTRL_INTERRUPT_ENABLE_REG (0x000)
  - **Binary Representation Diagram**: 
    ```
    31 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0
    0   O O O O O O O O O O O O Reset
    ```

- **Description**:
  - `PIDCTRL_INTERRUPT_ENABLE`: These bits are used to enable interrupt identification and processing. (R/W)

---

**Section Header:**
Register 13.2. PIDCTRL_INTERRUPT_ADDR_1_REG (0x004)

**Binary Representation Diagram for Register 13.2:**

- **Binary Representation**: 
  ```
  31 | O
  ```

- **Description**:
  - `PIDCTRL_INTERRUPT_ADDR_1_REG`: Level 1 interrupt vector entry address. (R/W)

---

**Section Header:**
Register 13.3. PIDCTRL_INTERRUPT_ADDR_2_REG (0x008)

**Binary Representation Diagram for Register 13.3:**

- **Binary Representation**: 
  ```
  31 | O
  ```

- **Description**:
  - `PIDCTRL_INTERRUPT_ADDR_2_REG`: Level 2 interrupt vector entry address. (R/W)

---

**Section Header:**
Register 13.4. PIDCTRL_INTERRUPT_ADDR_3_REG (0x00C)

**Binary Representation Diagram for Register 13.4:**

- **Binary Representation**: 
  ```
  31 | O
  ```

- **Description**:
  - `PIDCTRL_INTERRUPT_ADDR_3_REG`: Level 3 interrupt vector entry address. (R/W)

---

**Section Header:**
Register 13.5. PIDCTRL_INTERRUPT_ADDR_4_REG (0x010)

**Binary Representation Diagram for Register 13.5:**

- **Binary Representation**: 
  ```
  31 | O
  ```

- **Description**:
  - `PIDCTRL_INTERRUPT_ADDR_4_REG`: Level 4 interrupt vector entry address. (R/W)

---

**Footer Information:**
Espressif Systems  
Submit Documentation Feedback

**Document Version:** ESP32 TRM (Version 5.6)