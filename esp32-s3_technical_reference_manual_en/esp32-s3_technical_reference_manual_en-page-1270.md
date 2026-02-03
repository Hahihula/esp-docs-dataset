**Chapter Title:**
Chapter 34 SD/MMC Host Controller (SDHOST)

**Section Titles and Subsections with Content:**

### Section 34.3 - SD/MMC External Interface Signals

- **Introduction:** The primary external interface signals, which enable the SD/MMC controller to communicate with an external device.
- **Details of Signals:**
  - Clock signal (`sdhost_cclk_out_1[0]`)
  - Command signal (`sdhost_ccmd_out_1`)
  - Data signals (`sdhost_cdata_in_1[7:0]`, `sdhost_cdata_out_1[7:0]`)
- **Additional Signals:** Card interrupt, card detect, and write-protect.
- **Figure Reference:** Figure 34.3-1
- **Table Description (Table 34.3-1):** SD/MMC Signal Description

| Pin | Direction | Description |
|-----|-----------|-------------|
| sdhost_cclk_out | Output | Clock signals for slave device |
| sdhost_ccmd | Duplex | Duplex command/response lines |
| sdhost_cdata | Duplex | Duplex data read/write lines |
| sdhost_card_detect_n | Input | Card detection input line |
| sdhost_card_write_prt | Input | Card write protection status input |
| sdhost_rst_n | Output | Hardware reset for MMC4.4 cards |
| sdhost_ccmd_od_pullup_en | Output | Card Cmd Open-Drain Pullup |
| sdhost_card_int_n | Input | Interrupt pin for eSDIO devices |
| sdhost_data_strobe_n | Input | Card HS400 Data Strobe |

### Section 34.4 - Functional Description

#### Subsection: SD/MMC Host Controller Architecture (34.4.1)

- **Description:** The SD/MMC host controller consists of two main functional blocks, as shown in Figure.
- **Functional Blocks Details:**
  - Bus Interface Unit (BIU): Provides APB interfaces for registers, data access method for RAM, and DMA operation by DMA.
  - Card Interface Unit (CIU): Handles external memory card interface protocols. It also provides clock control.

**Footer Information:** 
- Company Name: Espressif Systems
- Document Version: ESP32-S3 TRM (Version 1.7)
- Page Number: 1270

**Navigation Links and Feedback Options:**
- GoBack button at the top right corner.
- Submit Documentation Feedback link.

(Note: The figure mentioned in Figure references is not described due to image limitations.)