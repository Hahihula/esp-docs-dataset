**Title:**
Chapter 15 Permission Control

**Subtitles and Body Texts with Descriptions of Registers:**

1. **Register 15.101. SYSCON_EXT_MEM_PMS_LOCK_REG (0x0020)**
   - Description:
     ```
     SYSCON_EXT_MEM_PMS_LOCK
     Set this bit to lock the permission configuration related to external memory.
     (R/W)
     ```
   - Diagram: 
     ```
     31    0
     0 O O O O O O O O O O O O O O O O Reset
     ```

2. **Register 15.102. SYSCON_FLASH_ACEn ATTR_REG (n: 0-3) (0x0028 + 4*n)**
   - Description:
     ```
     SYSCON_FLASH_ACEn ATTR
     Configures the permission to Region n of Flash.
     (R/W)
     ```
   - Diagrams and Labels for bits within register:

     - **Diagram:**
       ```
       31    0
       0 O O O O O O O O O O O O O O O Reset
       ```

     - **Diagram with Offset Label:**
       ```
       31    8   0
       0 O O O O O O O O O O O O O O Ox0ff
       ```

**Footer Information (Vertical Text):**

- ESP32-S3 TRM (Version 1.7)
- Submit Documentation Feedback

**Side Labels:**
- Espressif Systems on the left side.
- Chapter 15 Permission Control, Page number "796" and GoBack link at bottom right corner.

(Note: The text in red is part of register descriptions indicating specific attributes or functions.)