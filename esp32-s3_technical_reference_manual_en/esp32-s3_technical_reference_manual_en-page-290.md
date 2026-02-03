**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.207 EE.VUNZIP.16

**Subsection Headers and Content:**

- **Instruction Word:** 
  - `11 qs1[2:1]` | `1100 qs0[0]` | `qs0[2:0]` | `001110000100`

- **Assembler Syntax**
  - EE.VUNZIP.16 qs0, qs1

- **Description:** 
  This instruction implements the unzip algorithm on 16-bit vector data.

**Operation Table (Markdown format):**

```
 Operation
 qso[ 15: 0] = qs0[ 15: 0]
 qso[ 31: 16] = qs0[47:32]
 qso[ 47: 32] = qs0[79:64]
 qso[ 63: 48] = qs0[111:96]
 qso[ 79: 64] = qs1[15: 0]
 qso[ 95: 80] = qs1[47:32]
 qso[111: 96] = qs1[79:64]
 qso[127:112] = qs1[111:96]
 qs1[ 15: 0] = qs0[31: 16]
 qs1[ 31: 16] = qs0[63:48]
 qs1[ 47: 32] = qs0[95:80]
 qs1[ 63: 48] = qs0[127:112]
 qs1[ 79: 64] = qs1[31: 16]
 qs1[ 95: 80] = qs1[63:48]
 qs1[111: 96] = qs1[95: 80]
 qs1[127:112] = qs1[127:112]
```

**Footer Information:** 
- Espressif Systems
- Page number and document version information at the bottom right corner:
  - "290 ESP32-S3 TRM (Version 1.7)"
- Link for submitting documentation feedback is provided but not described in detail.

**Navigation:**
- A link labeled “GoBack” to navigate back, located near the top-right of the page header.