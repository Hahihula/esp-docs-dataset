**Chapter Title:**
Chapter 16 World Controller (WCL)

**Section Header:**
3

**Body Text with List Items and Descriptions:**

- Field WCL\Core_m_Current_1 is updated to 0, indicating CPU is no longer at the interrupt monitored at Entry 9. Instead, CPU is at the interrupt monitored at Entry 1 already.
  
- Fields WCL\Core_m_From_World_9 and WCL\Core_m_From_Entry_9 stay the same.

**Subsection Header:**
Other

**Body Text with List Items and Descriptions:**

- Other registers are not updated. 

**Section Numbering and Subsection Title:**
3. Then, when a new interrupt occurs at Entry 4 (highest priority), CPU executes to entry address of interrupt 4.
  
The World Switch Log Table is updated again as described in Figure 16.5-4:

**Figure Caption with Diagram Description:**
Figure 16.5-4. Nested Interrupts Handling - Entry 4

**Table Content:**

| current | from_entry | from_world |
|---------|------------|------------|
| 0       | 9          | 0          |
| 3       | 0          | 0          |
| 1       | 1          | 0          |

**Subsection Header and Description with List Items:**

- WCL\Core_m_Statusable4_Reg

  - Field WCL\Core_m_From_World_4 is updated to 0, indicating the CPU was in Secure World before this interrupt.
  
  - Field WCL\Core_m_From_Entry_4 is updated to 1, indicating the CPU was at Entry 1.

- Other registers are not updated. 

**Subsection Header:**
WCL\Core_m_Statusable1_Reg

**Body Text with List Items and Descriptions:**

- Field WCL\Core_m_Current_1 is updated to indicate that CPU is no longer monitored by interrupt entry, instead it was at the interrupt Entry 4 already.

- Fields are not updated. 

**Subsection Header:**
Other

**Body Text with List Items and Descriptions:**

- Other registers remain unchanged as described in previous points.
  
**Section Title:**
16.5.3 How to Read World Switch Log Registers

**Body Text Description of Steps for Reading the Logs (with reference figure):**

By reading World Switch Log Registers, we get information about world switches and nested interrupts.

Steps are detailed below:

- See Figure 16.5-4 as an example: 

**Footer Information with Document Reference:**  
Espressif Systems  
Submit Documentation Feedback

**Document Version Info at the Bottom Right Corner:**
ESP32-S3 TRM (Version 1.7)