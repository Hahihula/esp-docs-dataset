**Title: Chapter 34 SD/MMC Host Controller (SDHOST)**

---

**Figure Description:**  
*Figure 34.10-1. Clock Phase Selection*

**Diagram Explanation in Markdown Format:**
```
+---------------------------+
| bit[0]                   |
+---------------------------+
| clock_phase0              |
+---------------------------+
       |                             |
       |                             |
       v                             v
+---------------------------+ +---------------------------+
| MUX0                      | | MUX2                       |
+---------------------------+ +---------------------------+
| 0                         | | 0                          |
+---------------------------+ +---------------------------+
| clock_phase90             | | clk_out                     |
+---------------------------+ +---------------------------+
       ^                             ^
       |                             |
       v                             v
+---------------------------+ +---------------------------+
| clock_phase180            | | clock_phase270             |
+---------------------------+ +---------------------------+
       1                           1
```

**Text Explanation:**
This issue can be fixed by configuring register SDHOST_CLK_DIV_EDGE_REG. For example, set CCLKIN_EDGE_DRV_SEL bit to 0 to drive the output data in phase0, and set the CCLKIN_EDGE_SAM_SEL bit to 1 to select phase90 to sample the data from SDIO slave; if there are still timing issue, please set bit 4 or 6 to use phase180 or phase 270 to sample the data from SDIO slave.

Please find detailed information on the clock phase selection register SDHOST_CLK_DIV_EDGE_REG in Section Registers.

---

**Table Description:**
*Table 34.10-1. SDHOST Clk Phase Selection*

| Clock phase | phase_select value |
|-------------|--------------------|
| 0           | 0                  |
| 90          | 1                  |
| 180         | 4                  |
| 270         | 6                  |

---

**Subsection Title: 34.11 Interrupt**

**Text Explanation:**  
Interrupts can be generated as a result of various events. The SDHOST_IDSTS_REG register contains all the bits that might cause an interrupt. The SDHOST_IDINTEN_REG register contains an enable bit for each of the events that can cause an interrupt.

There are two groups of summary interrupts, "Normal" ones (bit8 SDHOST_IDSISTS_NIS) and "Abnormal" ones (bit9 SDHOST_IDSISTS_AIS), as outlined in the SDHOST_IDSISTS_REG register. Interrupts are cleared by writing 1 to the position of the corresponding bit. When all the enabled interrupts within a group are cleared, the

---

**Footer:**
Espressif Systems  
1280  
Submit Documentation Feedback  

ESP32-S3 TRM (Version 1.7)