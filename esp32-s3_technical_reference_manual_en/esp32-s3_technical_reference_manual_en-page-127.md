**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
18.51 EE.SRC.Q.LD.XP

**Subsection Titles and Content:**

- **Instruction Word:** 
  - Syntax: `11010000 qs1[2:0] O qu[2:0] qs0[1:0] OO ad[3:0] as[3:0] 111 qs0[2]`
  
- **Assembler Syntax**
  - Example: `EE.SRC.Q.LD.XP qu, as, ad, qs0, qs1`

- **Description:** 
  This instruction performs an arithmetic right shift on the 32-byte concatenation of registers qs0 and qs1 that hold the loaded data of two consecutive aligned addresses. By this way, you can obtain unaligned 16-byte data, which will be written to register qs0. The right shift amount is `SAR_BYTE` multiplied by 8.

- **Operation:**
  - Explanation:
    ```
    qs0[127:0] = {qs1[127:0], qs0[127:0]} >> {SAR_BYTE[3:0] << 3}
    qu[127:0] = load128({as[31:4],4{0}})
    as[31:0] = as[31:0] + ad[31:0]
    ```
  
**Footer Information:** 
- Company Name: Espressif Systems
- Document Version and Type: ESP32-S3 TRM (Version 1.7)
- Page Number: 127

**Navigation Links:**
- GoBack