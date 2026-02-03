**Chapter Title:**
Chapter 31 Two-wire Automotive Interface (TWAI®)

**Section Header with List Items:**
- The entire 11-bit ID
- RTR bit
- Data byte 1 (for filter only)
- EFF

**Body Text:**
The first 16 bits of the 29-bit ID.

The following Figure **31.5-3** illustrates how the 32-bit code and mask values will be interpreted in Dual Filter Mode.

**Figure Caption with Diagram Description:**
Figure 31.5-3. Dual Filter Mode

**Diagram Labels (from top to bottom):**
- ACR0 – Addr 0x0040
- AMR0 – Addr 0x0050
- SFF
- EF

**Table in Diagram for Filter 1:**
| ID | DB = Data Byte |
|----|---------------|
| 7 6 5 4 3 2 1 0| ACR1 – Addr 0x0044 |
|                | AMR1 – Addr 0x0054 |
|                | ACR3 – Addr 0x004C |

**Table in Diagram for Filter 2:**
| ID | DB = Data Byte |
|----|---------------|
| 7 6 5 4 3 2 1 0| ACR2 – Addr 0x0048 |
|                | AMR2 – Addr 0x0058 |
|                | ACR3 – Addr 0x004C |
|                | AMR3 – Addr 0x005C |

**Figure Caption with Diagram Description:**
Figure 31.5-3. Dual Filter Mode

**Subsection Title and Body Text:**

**Subtitle:** 
31.5.7 Error Management

**Body Text:**
The TWAI protocol requires that each TWAI node maintains the Transmit Error Count (TEC) and Receive Error Count (REC). The value of both error counts determines the current error state of the TWAI controller (i.e., Error Active, Error Passive, Bus-Off). The TWAI controller stores the TEC and REC values in the TWAI_TX_ERR_CNT_REG and TWAI_RX_ERR_CNT_REG respectively, and they can be read by the CPU anytime. In addition to the error states, the TWAI controller also offers an Error Warning Limit (EWL) feature that can warn the user of the occurrence of severe bus errors before the TWAI controller enters the Error Passive state.

**Footer:**
Espressif Systems

1208
ESP32-S3 TRM (Version 1.7)

Submit Documentation Feedback