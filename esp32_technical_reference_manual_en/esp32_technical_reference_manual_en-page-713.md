**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Section Header:**
GoBack

**Register Information for Register 29.56, PWM_FH2_CFG1_REG (0x00dc):**

- **Field Name:** PWM_FH2 FORCE OST  
  - Description: A toggle triggers a one-shot mode action.
  - Access Type: Read/Write
  - Binary Representation Diagram:
    ```
    3 | 4 | 5 | ... | 1 | 0 |
    ```

- **Field Name:** PWM_FH2 FORCE CBC  
  - Description: A toggle triggers a cycle-by-cycle mode action. 
  - Access Type: Read/Write

- **Field Name:** PWM_FH2 CBCPULSE  
  - Description: The cycle-by-cycle mode action refresh moment selection.
  - When bit0 is set to 1, TEZ; when bit1 is set to 1, TEP (Read/Write)

- **Field Name:** PWM_FH2 CLR OST  
  - Description: A toggle will clear on-going one-shot mode action. 
  - Access Type: Read/Write

**Register Information for Register 29.57, PWM_FH2_STATUS_REG (0x00e0):**

- **Field Name:** PWM_FH2 OST ON  
  - Description: Set and reset by hardware.
  - If set, a one-shot mode action is on-going.

- **Field Name:** PWM_FH2 CBC ON  
  - Description: Set and reset by hardware. 
  - If set, a cycle-by-cycle mode action is on-going (Read Only)

**Footer Information:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback

(Note: The binary representation diagrams are described based on the layout shown in the image.)