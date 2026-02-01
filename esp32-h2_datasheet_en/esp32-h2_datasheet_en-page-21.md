**Title: Figure 2-2. ESP32-H2 Power Scheme**

---

**Subtitle: 2.5.3 Chip Power-up and Reset**

Body Text:
Once the power is supplied to the chip, its power rails need a short time to stabilize. After that, CHIP_EN – the pin used for power-up and reset – is pulled high to activate the chip. For information on CHIP_EN as well as power-up and reset timing, see Figure 2-3 and Table 2-9.

---

**Subtitle: 2.8 VDDPST1/2, VDD3P3, VDDA_PMU, VBAT**

Table:
| Parameter | Description | Min (μs) |
|-----------|-------------|----------|
| t_STBL    | Time reserved for the power rails of VDDPST1, VDDPST2, VDD3P3, VDDA_PMU, and VBAT to stabilize before the CHIP_EN pin is pulled high to activate the chip | 50 |
| t_RST     | Time reserved for CHIP_EN to stay below V_TL_nRST to reset the chip (see Table 5-3) | 50 |

---

**Figure Caption: Figure 2-3. Visualization of Timing Parameters for Power-up and Reset**

---

**Table Caption: Table 2-9. Description of Timing Parameters for Power-up and Reset**

---

Footer:
Espressif Systems
Submit Documentation Feedback

ESP32-H2 Series Datasheet v1.2