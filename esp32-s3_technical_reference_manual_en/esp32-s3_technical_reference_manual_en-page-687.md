**Chapter Title:**
Chapter 15 Permission Control (PMS)

**GoBack Link:** [GoBack](#)

---

### Instruction Region:
- Then the Instruction Region should be only configured to be accessed by IBUS;
- And can be further split into three split regions by IRam0_split_line_0 and Iram0_split_line_1.

### Data Region:
- The Data Region should be only configured to be accessed by DBUS;
- And can be further split into three split regions by DRam0_split_line_0 and DRam0_split_line_1.

**See illustration in Figure 15.3-1 and Table 15.3-6 below:**

![Figure 15.3-1](#) Split Lines for Internal SRAM1

---

### Table Title:
Table 15.3-6. Internal SRAM1 Split Regions

| **Internal Memory** | **Instruction/Data Regions** | **Split Regions** |
| --- | --- | --- |
| SRAM1 | Instruction Region | Instr_Region_0 |
| &nbsp; | Instr_Region_1 | Instr_Region_1 |
| &nbsp; | Data Region | Data_Region_0 |
| &nbsp; | Data Region | Data_Region_1 |
| &nbsp; | Data Region | Data_Region_2 |

**A. See description below on how to configure the split lines.**

**B. Access to each split region can be configured independently. See details in Table 15.3-7 and 15.3-8.**

---

### Subtitle: Internal SRAM1 Split Regions

ESP32-S3 allows users to configure the split lines to their needs with registers below:

- **Split line** to split the Instruction and Data regions (IRam0_DRam0_split_line):
  - PMS_CORE_X_IRAM0_DRAM0_DMA_SPLIT_LINECONSTRAIN_1_REG
- The first split line to further split the Instruction Region (Iram0_split_line_0):
  - PMS_CORE_X_IRAM0_DRAM0_DMA_SPLIT_LINECONSTRAIN_2_REG
- **The second split line** to further split the Instruction Region (IRam0_split_line_1):
  - PMS_CORE_X_IRAM0_DRAM0_DMA_SPLIT_LINECONSTRAIN_3_REG

---

**Footer:**
Espressif Systems  
687 ESP32-S3 TRM (Version 1.7)  
[Submit Documentation Feedback](#)