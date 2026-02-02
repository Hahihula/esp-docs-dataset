**Title: Chapter 13 Process ID Controller (PID)**

---

### Register 13.11. PIDCTRL_LEVEL_REG (0x028)

| Bit | Description |
|-----|-------------|
| 4   | Reserved    |
| 3-0 | Reset       |

**Field:** PIDCTRL_CURRENT_STATUS  
The current status of the system. (R/W)  

---

### Register 13.12. PIDCTRL_FROM_n_REG (n: 1-7) (0x28+0x4*n)

| Bit | Description |
|-----|-------------|
| 6   | Reserved    |
| 5-0 | Reset       |

**Field:** PIDCTRL_PREVIOUS_STATUS_n  
System status before any of Level 1 to Level 6, NMI interrupts occur. (R/W)  

---

### Register 13.13. PIDCTRL_PID_NEW_REG (0x048)

| Bit | Description |
|-----|-------------|
| 2   | Reserved    |
| 1-0 | Reset       |

**Field:** PIDCTRL_PID_NEW  
New PID. (R/W)  

---

*Espressif Systems*  
*Submit Documentation Feedback*

ESP32 TRM (Version 5.6)

--- 

(Note: The "Reset" label is associated with the reset bits in each register, indicating that these are used to set all values of a bitfield back to their default state.)