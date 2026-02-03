**Title:**
Chapter 38 Pulse Count Controller (PCNT)

**Subtitles and Sections with Descriptions:**

1. **Register 38.10. PCNT_INT_CLR_REG (0x004C)**
   - Description of the register bits:
     ```
     PCNT_CNT_THR_EVENT_U1_INT_CLR
     PCNT_CNT_THR_EVENT_U2_INT_CLR
     PCNT_CNT_THR_EVENT_U3_INT_CLR
     PCNT_CNT_THR_EVENT_U4_INT_CLR
     (reserved)
     PCNT_CNT_THR_EVENT_U5_INT_CLR
     ```
   - Bit description:
     ```
     PCNT_CNT_THR_EVENT_U1_INT_CLR
     Set this bit to clear the PCNT_CNT_THR_EVENT_U1_INT in-
     terrupt. (WO)
     ```

2. **Register 38.11. PCNT_DATE_REG (0x00FC)**
   - Description of the register:
     ```
     PCNT_DATE
     This is the PCNT version control register. (R/W)
     ```
   - Hexadecimal value provided: `0x19072601`

**Footer Information:**
- Company Name: Espressif Systems
- Document Version and Type: ESP32-S3 TRM (Version 1.7)
- Page Number: 1452
- Link Texts:
  - Submit Documentation Feedback

**Navigation Links:**
- GoBack