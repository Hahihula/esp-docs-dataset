**Chapter Title:**
Chapter 4 Memory Management and Protection Units (MMU, MPU)

**Body Text:**
The layout of the pages in memory space is linear; namely, an SRAMO MMU page \( n \) covers address space 
\[0x40080000 + (\text{pagesizex}n)\] to \( 0x40080000 + (\text{pagesizex}(n+1)-1); \) similarly, an SRAM2 MMU page \( n \) covers 
\[0x3FFC0000 + (\text{pagesizex}n)\] to \( 0x3FFC0000 + (\text{pagesizex}(n+1)-1). \) Tables 4.3-5 and 4.3-6 show the resulting addresses in full.

**Table Title:**
Page 4.3-5. Page Boundaries for SRAMO MMU

**Table Structure (Markdown format):**

| **Page** | **8 KB Pages Bottom** | **4 KB Pages Bottom** | **2 KB Pages Bottom Top** |
|-----------|------------------------|------------------------|----------------------------|
| 0         | 40080000              | 40081FFF               | 40080000                   |
| 1         | 40082000              | 40083FFF               | 400807FF                    |
| 2         | 40084000              | 40085FFF               | 40080FFF                    |
| ...       | ...                    | ...                    | ...                        |
| Rest      | -                      | -                      | -                          |

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback