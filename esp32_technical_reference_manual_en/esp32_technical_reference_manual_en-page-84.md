**Chapter Title:**
Chapter 4 Memory Management and Protection Units (MMU, MPU)

**Table Titles with Descriptions:**

1. **Table 4.3-9. Virtual Address for External Memory**
   - Columns:
     - Name
     - Size
     - Low Boundary address
     - High Boundary address
     - Page quantity

2. **Table 4.3-10. MMU Entry Numbers for PRO_CPU**

3. **Table 4.3-11. MMU Entry Numbers for APP_CPU**

**Text Content:**
- External Flash:
  For flash, the relationships among entry numbers, virtual memory ranges, and PIDs are detailed in Tables 4.3-10 and 4.3-11, which for every memory region and PID combination specify the first MMU entry governing the mapping. This number refers to the MMU entry governing the very first page; the entire region is described by the amount of pages specified in the 'count' column.

These two tables are essentially the same, with the sole difference being that the APP_CPU entry numbers are 2048 higher than the corresponding PRO_CPU numbers. Note that memory regions VAddr0 and VAddr1 are only accessible using PID O and I, while VAddr can only be accessed by PID 2 ~ 7.

**Additional Information:**
- As these tables show, virtual address VAddr1 can only be used by processes with a PID of 0 or 1. There is an Espressif Systems ESP32 TRM (Version 5.6) Submit Documentation Feedback page at the bottom.
  
(Note: The text content includes explanations and notes about memory management in relation to external flash, MMU entry numbers for PRO_CPU and APP_CPU.)