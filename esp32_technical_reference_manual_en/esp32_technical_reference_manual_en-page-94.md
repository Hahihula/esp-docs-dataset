**Chapter Title:**
Chapter 5 eFuse Controller (EFUSE)

**Section Header:**
GoBack

**Body Text:**

The column “Software-Read-Protection by efuse_rd.disable” in Table 5.3-1 lists the corresponding bits in efuse_rdDisable that determine the software read-protection status of the six system parameters. If a bit in the system parameter efuse_rd_disable is 0, the system parameter controlled by the bit is not software-read-protected. If a bit in the system parameter efuse_rd_disable is 1, the system parameter controlled by the bit is software-read-protected. If a system parameter is software-read-protected, it will remain in this state.

**Subsection Title:**
5.3.1.3 System Parameter coding_scheme

**Body Text:**

As Table 5.3-1 shows, only three system parameters, BLOCK1, BLOCK2, and BLOCK3, have variable bit widths. Their bit widths are controlled by another system parameter, coding_scheme. Despite their variable bit widths, BLOCK1, BLOCK2, and BLOCK3 are assigned a fixed number of bits in eFuse. There is an encoding mapping between these three system parameters and their corresponding stored values in eFuse. For details please see Table 5.3-2.

**Table Title:**
Table 5.3-2. BLOCK1/2/3 Encoding

| coding_scheme[1:0] | Width of BLOCK1/2/3 | Coding scheme | Number of bits in eFuse |
|--------------------|-----------------------|--------------|-------------------------|
| 00/11              | 256                   | None         | 256                     |
| 01                 | 192                   | 3/4          | 256                     |
| 10                 | 128                   | Repeat       | 256                     |

**Body Text:**

The three coding schemes are explained as follows:

- BLOCKN represents any of the following three system parameters: BLOCK1, BLOCK2 or BLOCK3.
- BLOCKN[255 : 0], BLOCKN[191 : 0], and BLOCKN[127 : 0] represent each bit of the three system parameters in the three encoding schemes.

- eBLOCKN[255:0] represents each corresponding bit of those system parameters in eFuse after being encoded.
  
**Mathematical Expressions:**

None

**Additional Mathematical Expression (3/4):**
\[
\text{BLOCKN}^j_i[7 : 0] = \text{BLOCKN}[48i + 8j + i : 48i + 8j]
\]

**Additional Mathematical Expression for eBLOCKN:**
For \( i \in \{0,1,2,3\} \), 
\[
e^{BLOCKN}_i^j[7 : 0] = e^{BLOCKN}[64i + 8j + 7 : 64i + 8j]
\]

**Additional Mathematical Expression (For i ∈ {0,1,2,3}, j ∈ {0,1,...}):**
\[
e^{BLOCKN}_i^j[7 : 0] = \text{BLOCKN}[7 : 0] 
\]

**Additional Mathematical Expressions:**

- For \( j = 6 \):
  \[
  e^{BLOCKN}_i^j[7 : 0] = \sum_{k=0}^{5}(l + 1) \cdot \text{BLOCKN}_i^j[k], \quad l = 7
  \]

- For \( j = 7 \):
  \[
  e^{BLOCKN}_i^j[7 : 0] = \sum_{k=0}^{5}(l + 1) \cdot \text{BLOCKN}_i^j[k], \quad l = 6
  \]

**Additional Information:**
Espressif Systems

94 ESP32 TRM (Version 5.6)

Submit Documentation Feedback