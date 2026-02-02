**Title: Boot Configurations**

---

### Table 4-7. JTAG Signal Source Control

| **JTAG Signal Source** | eFuse1^2 | eFuse2^3 | eFuse3^4 | GPIO7 |
|------------------------|-----------|----------|----------|-------|
| USB Serial/JTAG Controller | O | - | X | 1 |
| JTAG pins MTDI, MTCK, MTMS, and MDIO | x | - | - | 0 |
| USB Serial/JTAG Controller^6 | - | 1 | X | - |
| JTAG is disabled | 1 | - | - | X |

**Footnotes:**
1. Bold marks the default value and configuration.
2. eFuse 1: EFUSE_DIS_PAD_JTAG
3. eFuse 2: EFUSE_DIS_USB_JTAG
4. eFuse 3: EFUSE_JTAG_SEL_ENABLE
5. x: indicates that the value has no effect on the result and can be ignored.

**Additional Information:**  
In Joint Download Boot 1 mode, the USB Serial/JTAG controller is forcibly disabled, and the JTAG signal only comes from JTAG pins. If PAD_JTAG is also disabled, then JTAG is disabled.

---

### Section: Chip Power-up and Reset

Once the power is supplied to the chip, its power rails need a short time to stabilize. After that, CHIP_PU – the pin used for power-up and reset should be pulled high to activate the chip. For information on CHIP_PU as well as power-up and reset timing, see Figure 4-2 and Table 4-8.

**Figure:**  
[Visualization of Timing Parameters for Power-up and Reset](#)

---

### Table 4-8. Description of Timing Parameters for Power-up and Reset

| **Parameter** | **Description** | Min (µs) |
|----------------|------------------|----------|
| t_STBL | Time reserved for the power rails of VDDPST1, VDDPST2, VDDA1, VDDA2, VDDA3, VDDA4, VDDA5, VDDA6, VDDA7, and VDDA8 to stabilize before the CHIP_PU pin is pulled high to activate the chip | 50 |
| t_RST | Time reserved for CHIP PU to stay below V_IL-nRST to reset the chip (see Table 6-3) | 50 |

---

**Footer:**  
Espressif Systems  
20 ESP32-C5-WROOM-1 & WROOM-1U Datasheet v0.8  
Submit Documentation Feedback  
PRELIMINARY