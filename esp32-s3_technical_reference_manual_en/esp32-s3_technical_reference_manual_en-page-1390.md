**Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Register Information:**
- Register Name: MCPWM_FH1_CFGO_REG (0x0CA0)
- Bit Positions and Values:
  - 31 to 24, Reserved.
  - 23 down to bit positions with values ranging from '0' to 'F', indicating various configurations for different PWM channels.

**Table of Registers:**
1. **MCPWM_FH1_SW_CBC (Enable register for software force cycle-by-cycle mode action)**
   - Description:
     ```
     1: enable.
     0: disable,
     ```
   - Access Type: Read/Write

2. **MCPWM_FH1_F2_CBC (event_f2 will trigger cycle-by-cycle mode action)**
   - Description:
     ```
     0: disable, 1: enable.
     ```
   - Access Type: Read/Write

3. **MCPWM_FH1_F1_CBC (event_f1 will trigger cycle-by-cycle mode action)**
   - Description:
     ```
     0: disable, 1: enable,
     ```
   - Access Type: Read/Write

4. **MCPWM_FH1_FO_CBC (event_f0 will trigger cycle-by-cycle mode action)**
   - Description:
     ```
     0: disable, 1: enable.
     ```
   - Access Type: Read/Write

5. **MCPWM_FH1_SW_OST (Enable register for software force one-shot mode action)**
   - Description:
     ```
     0: disable, 1: enable,
     ```
   - Access Type: Read/Write

6. **MCPWM_FH1_F2_OST (event_f2 will trigger one-shot mode action)**
   - Description:
     ```
     0: disable, 1: enable.
     ```
   - Access Type: Read/Write

7. **MCPWM_FH1_F1_OST (event_f1 will trigger one-shot mode action)**
   - Description:
     ```
     0: disable, 1: enable.
     ```
   - Access Type: Read/Write

8. **MCPWM_FH1_FO_OST (event_f0 will trigger one-shot mode action)**
   - Description:
     ```
     0: disable, 1: enable,
     ```
   - Access Type: Read/Write

9. **MCPWM_FH1_A_CBC_D (Cycle-by-cycle mode action on PWM1A when fault event occurs and timer is decreasing.)**
   - Description for different values of the bit:
     - `0`: do nothing
     - `1`: force low, 2: force high, 3: toggle.
   - Access Type: Read/Write

10. **MCPWM_FH1_A_CBC_U (Cycle-by-cycle mode action on PWM1A when fault event occurs and timer is increasing.)**
    - Description for different values of the bit:
      - `0`: do nothing
      - `1`: force low, 2: force high, 3: toggle.
    - Access Type: Read/Write

11. **MCPWM_FH1_A_OST_D (One-shot mode action on PWM1A when fault event occurs and timer is decreasing.)**
    - Description for different values of the bit:
      - `0`: do nothing
      - `1`: force low, 2: force high, 3: toggle.
    - Access Type: Read/Write

12. **MCPWM_FH1_A_OST_U (One-shot mode action on PWM1A when fault event occurs and timer is increasing.)**
    - Description for different values of the bit:
      - `0`: do nothing
      - `1`: force low, 2: force high, 3: toggle.
    - Access Type: Read/Write

13. **MCPWM_FH1_B_CBC_U (Cycle-by-cycle mode action on PWM1B when fault event occurs and timer is increasing.)**
    - Description for different values of the bit:
      - `0`: do nothing
      - `1`: force low, 2: force high, 3: toggle.
    - Access Type: Read/Write

14. **MCPWM_FH1_B_OST_D (One-shot mode action on PWM1B when fault event occurs and timer is decreasing.)**
    - Description for different values of the bit:
      - `0`: do nothing
      - `1`: force low, 2: force high, 3: toggle.
    - Access Type: Read/Write

15. **MCPWM_FH1_B_OST_U (One-shot mode action on PWM1B when fault event occurs and timer is increasing.)**
    - Description for different values of the bit:
      - `0`: do nothing
      - `1`: force low, 2: force high, 3: toggle.
    - Access Type: Read/Write

**Footer Information:**
- Company Name: Espressif Systems
- Document Version and Page Number: ESP32-S3 TRM (Version 1.7), page number not specified in the provided text.

**Link for Documentation Feedback:** Submit Documentation Feedback