**Title: Boot Configurations**

---

### Table 4-5. JTAG Signal Source Control

| **JTAG Signal Source** | EFUSE_DIS_PAD_JTAG | EFUSE_DIS_USB_JTAG | EFUSE_STRAP_JTAG_SEL | GPIO3 |
|-------------------------|----------------------|---------------------|------------------------|-------|
| USB Serial/JTAG Controller | 0                   | O                   | Ignored                | 1     |
| JTAG pins               | 1                   | O                   | Ignored                | Ignored |
|                         | 0                   | 0                   | Ignored                | 0     |
| JTAG is disabled        | 0                   | 1                   | Ignored                | Ignored |

**Notes:**
1. Bold marks the default value and configuration.
2. JTAG pins refer to MTDI, MTCK, MTMS, and MTDO.

---

### Section Title

#### Subtitle:

4.5 Chip Power-up and Reset

---

Once the power is supplied to the chip, its power rails need a short time to stabilize. After that, EN – the pin used for power-up and reset - is pulled high to activate the chip. For information on EN as well as power-up and reset timing, see Figure 4-2 and Table 4-6.

---

**Figure Caption:**

Figure 4-2. Visualization of Timing Parameters for Power-up and Reset

---

### Subtitle:

#### Description:
Table 4-6. Description of Timing Parameters for Power-up and Reset

| **Parameter** | **Description** | **Min (µs)** |
|---------------|------------------|--------------|
| t_STBL        | Time reserved for the power rails of VDDA, VDD3P3, VDD3P3_RTC, and VDD3P3_CPU to stabilize before the EN pin is pulled high to activate the chip. | 50 |
| t_RST         | Time reserved for EN to stay below V_IL_nRST to reset the chip (see Table 6-3). | 50 |

---

**Footer:**

Espressif Systems  
Page number: 16  
Submit Documentation Feedback

---

**Document Title:** ESP32-S3-MINI-1 & MINI-1U Datasheet v1.6