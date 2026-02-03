**Chapter Title:**
Chapter 34 SD/MMC Host Controller (SDHOST)

**GoBack Link:** GoBack

**Register Information:**
- **Register Name and Address:** Register 34.41, SDHOST_CLK_DIV_EDGE_REG (0x800)
- **Bit Positions with Labels in Parentheses:**
  - [32] (reserved)
  - [24] 
  - [23]
  - [22]
  - [21]
  - [20]
  - [17]
  - [16]
  - [15]
  - [14]
  - [13]
  - [12]
  - [9]
  - [8]
  - [6]
  - [5]
  - [3] (SDHOST_CLK_EDGE_DRV_SEL)
  - [2]
  - [0]

**Bit Values:**
- Reset
- 0x000, OXO, Ox1

**Description of Bits and their Functions in Markdown format with headings for clarity:**


### SDHOST_CLK_SOURCE_REG
- **Function Description:** Set to 1 to use 160M PLL clock. Set to 0 to use 40M XLTAL clock.
- **Access Type:** (R/W)

### CCLKIN_EDGE_N
- **Description:** This value should be equal to CCLKIN_EDGE_L.
- **Access Type:** (R/W)

### CCLKIN_EDGE_L, CCLKIN_EDGE_H
- **Function Description:** The low level of the divider clock. The high level of the divider clock respectively; their values are larger than or smaller than that in `CCLKIN_EDGE_N`.
- **Access Type:** (R/W) for both

### CCLKIN_EDGE_SLF_SEL, CCLKIN_EDGE_SAM_SEL
- **Function Description:** Used to select the clock phase of internal signal from phase90, phase180, or phase270.
- **Access Type:** (R/W)

### CCLKIN_EDGE_DRV_SEL
- **Function Description:** Used to select the clock phase of output signal from phase90, phase180, or phase270.

**Note:**
SD/MMC use this register to divide 160M clock(CCLKIN_EDGE_H/CCLKIN_EDGE_L). The output clock connect to sdio slave divider by this register and SDHOST_CLKDIV_REG; there are four clock source selected by SDHOST_CLKSRC_REG register. 

**Footer Information:** 
- **Company Name:** Espressif Systems
- **Page Number:** 1309
- **Document Version:** ESP32-S3 TRM (Version 1.7)
- **Link for Submitting Documentation Feedback:** [Submit Documentation Feedback](#)