**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Link:**
GoBack

**Section Title:**
1.8.209 EE.VUNZIP.8

**Subsection Titles and Content:**

- **Instruction Word:** 
  - `11 qs1[2:1] 1100 qs0[0] qs0[2:0] 001110100100`

- **Assembler Syntax**
  - EE.VUNZIP.8 qs0, qs1

- **Description**
  - This instruction implements the unzip algorithm on 8-bit vector data.

**Subsection Title and Content (List of Operations):**

- Operation
  ```
  qs0[7:0] = qs0[7:0]
  qs0[15:8] = qs0[23:16]
  qs0[23:16] = qs0[39:32]
  qs0[31:24] = qs0[55:48]
  qs0[39:32] = qs0[71:64]
  qs0[47:40] = qs0[87:80]
  qs0[55:48] = qs0[103:96]
  qs0[63:56] = qs0[119:122]
  qs0[71:64] = qs1[7:0]
  qs0[79:72] = qs1[23:16]
  qs0[87:80] = qs1[39:32]
  qs0[95:88] = qs1[55:48]
  qs0[103:96] = qs1[71:64]
  qs0[111:104] = qs1[87:80]
  qs0[119:122] = qs1[103:96]
  qs0[127:120] = qs1[119:122]
  qs1[7:0] = qs1[15:8]
  qs1[15:8] = qs1[31:24]
  qs1[23:16] = qs1[47:40]
  qs1[31:24] = qs1[63:56]
  qs1[39:32] = qs1[79:72]
  qs1[47:40] = qs1[95:88]
  qs1[55:48] = qs1[111:104]
  qs1[63:56] = qs1[127:120]
  qs1[71:64] = qs1[15:8]
  qs1[79:72] = qs1[31:24]
  qs1[87:80] = qs1[47:40]
  qs1[95:88] = qs1[63:56]
  qs1[103:96] = qs1[79:72]
  qs1[111:104] = qs1[95:88]
  qs1[119:122] = qs1[111:104]
  qs1[127:120] = qs1[127:120]
  ```

**Footer Information:**
- Espressif Systems
- Page number and document version information:
  - "292 ESP32-S3 TRM (Version 1.7)"
- Link for feedback or submission of documentation issues.
  - Submit Documentation Feedback