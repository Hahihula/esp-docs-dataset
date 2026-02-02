**Title: Chapter 25 Two-Wire Automotive Interface (TWAI)**

---

### Figure Caption:
Figure 25.5-3. Dual Filter Mode

---

#### Definitions in Diagrams:

- **ID = Identifier**
- **ACR = TWAI_ACCEPTANCE_CODE**
- **DB = Data Byte**
- **AMR = TWAI ACCEPTANCE_MASK**

---

**Subsection: Error Passive (Section Title)**

25.5.7.2 Error Passive
----------------------
The TWAI controller is in the Error Passive state when the TEC or REC value exceeds 127. Likewise, when both the TEC and REC are less than or equal to 127, the TWAI controller enters the Error Active state. The Error Passive Interrupt is triggered whenever the TWAI controller transitions from the Error Active state to the Error Passive state or vice versa.

---

**Subsection: Bus-Off and Bus-Off Recovery (Section Title)**

25.5.7.3 Bus-Off and Bus-Off Recovery
--------------------------------------
The TWAI controller enters the Bus-Off state when the TEC value exceeds 255. On entering the Bus-Off state, the TWAI controller will automatically do the following:

---

**Footer:**
Espressif Systems  
Submit Documentation Feedback

ESP32 TRM (Version 5.6)  

--- 

### Diagram Details:
The diagram shows two filter modes with multiple registers and data bytes labeled as follows for each register in both Filter 1 and Filter 2.

- **Filter 1** includes ACR0, AMR0, ACR1, AMR1.
- **Filter 2** includes ACR2, AMR2. 

Each entry shows a sequence of bits (e.g., "7 6 5 4 3 2 1 0") for each register.

### Example Entries:
- For Filter 1: 
  - ACR0 – Addr 0x0040
    - DB entries like DB.8, DB.9,...DB.1.
  
- For Filter 2:
  - AMR2 – Addr 0x0058
    - DB entries similar to the previous example.

Each entry is structured with a sequence of bits corresponding to different data bytes (DB) and registers in hexadecimal format followed by their addresses or values, such as "7 6 5 4 3 2 1 0".