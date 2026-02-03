**Title: Chapter 15 Permission Control (PMS)**

---

**Table Title:** Table 15.4-1 – cont’d from previous page  
**Subtitle:** Peripherals  

| **Peripherals** | Secure World | Non-secure World | Bit^3 |
|----------------|--------------|------------------|-------|
| USB OTG Core   | PIF_PMS CONSTRAIN_4_REG | PIF_PMS CONSTRAIN_8_REG [15:14] |
| USB OTG External | PIF_PMS CONSTRAIN_4_REG | PIF_PMS CONSTRAIN_8_REG [3:2] |
| Two-wire Automotive Interface | PIF_PMS CONSTRAIN_3_REG | PIF_PMS CONSTRAIN_7_REG [11:10] |
| UHCI 0         | PIF_PMS CONSTRAIN_6_REG [7:6] |
| SD/MMC Host Controller | PIF_PMS CONSTRAIN_3_REG | PIF_PMS CONSTRAIN_7_REG [9:8] |
| LED PWM Controller | PIF_PMS CONSTRAIN_2_REG | PIF_PMS CONSTRAIN_6_REG [17:16] |
| Motor Control PWM 0   | PIF_PMS CONSTRAIN_2_REG | PIF_PMS CONSTRAIN_6_REG [25:24] |
| Motor Control PWM 1   | PIF_PMS CONSTRAIN_3_REG | PIF_PMS CONSTRAIN_7_REG [13:12] |
| Remote Control Peripheral | PIF_PMS CONSTRAIN_2_REG | PIF_PMS CONSTRAIN_6_REG [11:10] |
| Camera-LCD Controller  | PIF_PMS CONSTRAIN_4_REG | PIF_PMS CONSTRAIN_8_REG [11:10] |
| APB Controller     | PIF_PMS CONSTRAIN_7_REG [5:4] |
| ADC Controller     | PIF_PMS CONSTRAIN_8_REG [9:8] |

**Section Title:** 15.4.2 Split Peripheral Regions into Split Regions

Each of ESP32-S3’s peripheral region can be further split into 11 regions (from Peri Region0 ~ Peri Region10) for more flexible permission control.

For example, the registers for ESP32-S3's GDMA controller are allocated as:
- 5 sets of registers for 5 of each RX channel
- 5 sets of registers for 5 of each TX channel
- 1 set of registers for configuration

As seen above, GDMA’s peripheral region is divided into 11 split regions (implemented in hardware), which can be configured with different permission independently, thus achieving independent permission control to each GDMA channel.

Users can configure CPU’s read (R) and write (W) accesses to a specific split region (Peri Region^r) from the Secure World and the Non-secure World by configuring PMS_CORE_m_Region_PMS CONSTRAIN_n_REG. Note that permission can be configured independently for CPU0 and CPU1.

**Notes on PMS CORE m_Region PMS CONSTRAIN n_REG:**
- `m` can be 0 or 1 for CPU0 and CPU1 respectively.
- `n` can be 1~14, in which:
  - Region_PMS CONSTRAIN_1_REG is for configuring CPU’s permission from the Secure World.
  - Region_PMS CONSTRAIN_2_REG is for configuring CPU's permission from the Non-secure World.
  - Region_PMS CONSTRAIN_n_REG (n = 3~14) are used to configuring the starting addresses for each Peri Regions. Note the starting address of each Peri Region is also the ending address of the previous Peri Region.

---

**Footer:**  
Espressif Systems  
695  
ESP32-S3 TRM (Version 1.7)  

[Submit Documentation Feedback](#)