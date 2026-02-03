**Chapter Title:**
Chapter 15 Permission Control (PMS)

**Table Title and Content:**
- **Title:** Table 15.4-2. Access Configuration of Peri Regions

| Peri Regions | Starting Address Configuration | Secure World | Non-secure World |
|--------------|----------------------------------|--------------|-------------------|
| Peri Region0 | Region_PMS CONSTRAIN_3_REG      | Region_PMS CONSTRAIN_1_REG [1:0] | Region_PMS CONSTRAIN_2_REG [1:0] |
| Peri Region1 | Region_PMS CONSTRAIN_4_REG      | Region_PMS CONSTRAIN_1_REG [3:2] | Region_PMS CONSTRAIN_2_REG [3:2] |
| Peri Region2 | Region_PMS CONSTRAIN_5_REG      | Region_PMS CONSTRAIN_1_REG [5:4] | Region_PMS CONSTRAIN_2_REG [5:4] |
| Peri Region3 | Region_PMS CONSTRAIN_6_REG      | Region_PMS CONSTRAIN_1_REG [7:6] | Region_PMS CONSTRAIN_2_REG [7:6] |
| Peri Region4 | Region_PMS CONSTRAIN_7_REG      | Region_PMS CONSTRAIN_1_REG [9:8] | Region_PMS CONSTRAIN_2_REG [9:8] |
| Peri Region5 | Region_PMS CONSTRAIN_8_REG      | Region_PMS CONSTRAIN_1_REG [11:10]| Region_PMS CONSTRAIN_2_REG [11:10]|
| Peri Region6 | Region_PMS CONSTRAIN_9_REG      | Region_PMS CONSTRAIN_1_REG [13:12]| Region_PMS CONSTRAIN_2_REG [13:12]|
| Peri Region7 | Region_PMS CONSTRAIN_10_REG     | Region_PMS CONSTRAIN_1_REG [15:14]| Region_PMS CONSTRAIN_2_REG [15:14]|
| Peri Region8 | Region_PMS CONSTRAIN_11_REG     | Region_PMS CONSTRAIN_1_REG [17:16]| Region_PMS CONSTRAIN_2_REG [17:16]|
| Peri Region9 | Region_PMS CONSTRAIN_12_REG     | Region_PMS CONSTRAIN_1_REG [19:18]| Region_PMS CONSTRAIN_2_REG [19:18]|
| Pen Region0 | Region_PMS CONSTRAIN_13_REG     | Region_PMS CONSTRAIN_1_REG [21:20]| Region_PMS CONSTRAIN_2_REG [21:20]|

**Section Title and Content:**
- **Title:** 15.5 External Memory
- **Body Text:** ESP32-S3 can access the external memory via one of the three ways illustrated in Figure 15.5-1 below.
  - CPU via SPI1
  - CPU via CACHE
  - GDMA

**Figure Description:**
- **Title:** Figure 15.5-1. Three Ways to Access External Memory
- The figure illustrates a block diagram showing the interaction between CPU, Cache, MMU, SPI0/1, and flash memory.

**Additional Information in Section Title:**
- "SPI1, CACHE or GDMA must be configured with specific permission before accessing external memory."

**Subsection Title and Content:**
- **Title:** 15.5.1 Address
- Both ESP32-S3's flash and SRAM can be further split to achieve more flexible permission control. Each split region can be configured with different access independently.
  - Flash can be split into 4 regions, the length of each should be the integral multiples of 64 KB.

**Footer:**
- "Espressif Systems"
- Page number and document version information:
  - **Page Number:** 696
  - **Document Version:** ESP32-S3 TRM (Version 1.7)
  
**Action Links:**
- Submit Documentation Feedback