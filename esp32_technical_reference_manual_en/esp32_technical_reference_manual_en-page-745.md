**Chapter Title:**
Chapter 31 On-Chip Sensors and Analog Signal Processing

**GoBack Link:** [GoBack](#)

**Body Text:**

There are three scanning modes:
- Single mode, double mode, alternate mode.

ESP32 supports up to a 12-bit SAR ADC resolution. The data in DMA is composed of the ADC result plus some necessary information related to the scanning mode:

For single mode (4-bit channel selection added).
For double or alternate mode: 
   - For Type I:
      - Resolution can be as high as 12 bits.
   - For Type II:
      - Resolution up to 15 bits.

**Tables and Descriptions:**

- **Table Title:** Table 31.3-4. Fields of Type I DMA Data Format
  - **Columns:** ch_sel[3:0], data[11:0]
  - **Rows:** channel, SAR ADC data

- **Table Title:** Table 31.3-5. Fields of Type II DMA Data Format
  - **Columns:** ch_sel[3:0], data[10:0]
  - **Rows:** sar_sel, SAR ADC data; SAR ADCn, channel
  
**Additional Information about DACs and Features (Sections):**

**Section Title:** 31.4 DAC

- **Subsection Title:** 31.4.1 Introduction
  - Description of dual DAC channels used for converting digital values into analog output signals.

- **Subsection Title:** 31.4.2 Features
  - Two features:
     - Two 8-bit DAC channels.
  
**Footer:**
Espressif Systems, Page number (745), ESP32 TRM (Version 5.6) with links to Submit Documentation and Feedback.

**Navigation Links at the Bottom:** [Submit Documentation](#) | [Feedback](#)