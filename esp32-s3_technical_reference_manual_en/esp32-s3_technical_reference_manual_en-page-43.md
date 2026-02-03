**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Figure Captions and Descriptions:**

- **Figure Caption:** Figure 1.4-3.
- **Description of the first figure:** EE.ZERO.GACC in Little-Endian Byte Order

    - **Diagram Description for First Figure:**
        ```
        Byte order
        23 22 21 20 19 18 17 16 15 14 13 12 11 10 9 8 7 6 5 4 3 2 1 0
        
        Most-significant byte
        Instruction code: 0 0 1 0 0 1 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
        
        Least-significant byte
        ```

- **Figure Caption:** Figure 1.4-4.
- **Description of the second figure:** EE.ZERO.QACC in Big-Endian Byte Order

    - **Diagram Description for Second Figure:**
        ```
        Byte order
        7 6 5 4 3 2 1 0 15 14 13 12 11 10 9 8 23 22 21 20 19 18 17 16
        
        Most-significant byte
        Instruction code: 0 1 0 0 1 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1
        
        Least-significant byte
        ```

**Subsection Title:**
1.4.2 Instruction Field Definition

**Body Text:**
Table 1.4-1 provides the meaning of the characters covered in instruction descriptions. You can find such characters and corresponding descriptions in Section 1.8.

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback