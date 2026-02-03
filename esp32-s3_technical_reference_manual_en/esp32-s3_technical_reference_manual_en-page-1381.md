**Title: Chapter 36 Motor Control PWM (MCPWM)**

**Register Information:**  
- **Register Name**: MCPWM_FHO_CFGO_REG  
- **Address**: 0x0068  

**Table Description:**  
The table lists various registers related to the MCPWM module, each with a specific function and bit positions. The columns include register names (e.g., MCPWM_FHO_Bca Ost U), address ranges for different bits within those registers.

**Register Descriptions:**

1. **MCPWM_FHO_SW_CBC**
   - Function: Enable register for software force cycle-by-cycle mode action.
   - Bits 31-0:
     - `0`: disable
     - `1`: enable

2. **MCPWM_FHO_F2_CBC**
   - Function: Trigger cycle-by-cycle mode action when event_f2 occurs.

3. **MCPWM_FHO_E1_CBC**
   - Function: Trigger cycle-by-cycle mode action when event_f1 occurs.
   - Bits 0-7:
     - `0`: disable
     - `1`: enable

4. **MCPWM_FHO_FO_CBC**
   - Function: Trigger cycle-by-cycle mode action for software force one-shot mode.

5. **MCPWM_FHO_SW_OST**
   - Function: Enable register for software force one-shot mode.
   - Bits 0-7:
     - `0`: disable
     - `1`: enable

6. **MCPWM_FHO_F2_OST**
   - Function: Trigger one-shot mode action when event_f2 occurs.

7. **MCPWM_FHO_F1_OST**
   - Function: Trigger one-shot mode action for software force cycle-by-cycle.
   - Bits 0-7:
     - `0`: disable
     - `1`: enable

8. **MCPWM_FHO_FO_OST**
   - Function: Trigger one-shot mode action when event_f0 occurs.

9. **MCPWM_FHO_A_CBC_D**
   - Function: Cycle-by-cycle mode action on PWMOA during fault events.
   - Bits 0-7:
     - `0`: do nothing
     - `1`: force low, `2`: force high, `3`: toggle

10. **MCPWM_FHO_A_CBC_U**
    - Function: Cycle-by-cycle mode action on PWMOA during fault events.
    - Bits 0-7:
      - `0`: do nothing
      - `1`: force low, `2`: force high, `3`: toggle

11. **MCPWM_FHO_A_OST_D**
    - Function: One-shot mode action on PWMOA during fault events.
    - Bits 0-7:
      - `0`: do nothing
      - `1`: force low, `2`: force high, `3`: toggle

12. **MCPWM_FHO_A_OST_U**
    - Function: One-shot mode action on PWMOA during fault events.
    - Bits 0-7:
      - `0`: do nothing
      - `1`: force low, `2`: force high, `3`: toggle

13. **MCPWM_FHO_B_CBC_D**
    - Function: Cycle-by-cycle mode action on PWMOB during fault events.
    - Bits 0-7:
      - `0`: do nothing
      - `1`: force low, `2`: force high, `3`: toggle

14. **MCPWM_FHO_B_CBC_U**
    - Function: Cycle-by-cycle mode action on PWMOB during fault events.
    - Bits 0-7:
      - `0`: do nothing
      - `1`: force low, `2`: force high, `3`: toggle

15. **MCPWM_FHO_B_OST_D**
    - Function: One-shot mode action on PWMOB during fault events.
    - Bits 0-7:
      - `0`: do nothing
      - `1`: force low, `2`: force high, `3`: toggle

16. **MCPWM_FHO_B_OST_U**
    - Function: One-shot mode action on PWMOB during fault events.
    - Bits 0-7:
      - `0`: do nothing
      - `1`: force low, `2`: force high, `3`: toggle

**Footer:**  
Espressif Systems  
Page number and document version information.