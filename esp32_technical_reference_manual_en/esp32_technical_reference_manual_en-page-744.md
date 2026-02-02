**Chapter Title:**
Chapter 31 On-Chip Sensors and Analog Signal Processing

**Body Text:**

- Multiple-channel scanning mode; there is a pattern table that defines the measurement rule for each SAR ADC. The scanning mode can be configured as a single mode, double mode, or alternate mode.
  
- The scanning can be started by software or I2S.

- DMA support; an interrupt will be generated when scanning is finished.

**Note:**
We do not use the term "start of conversion" in this section, because there is no direct access to starting a single SAR analog-to-digital conversion. We use “start of scan” instead, which implies that we expect to scan a sequence of channels with DIG ADC controllers.

**Figure Caption and Description:**

- **Figure 31.3-4 shows a diagram of DIG SAR ADC controllers.**
  
  - The figure includes various components such as "DIG SAR ADC Control Top," pointers labeled “pointer,” pattern table, S/W or HW Event Trigger start of scan, pad_en / bit_width / atten for different channels (SAR ADC1 CTRL and SAR ADC2 CTRL), mode select with options like“16 bits”and“option”, DMA interrupt.

**Additional Text:**

The pattern tables contain the measurement rules mentioned above. Each table has 16 items which store information on channel selection, resolution and attenuation. When scanning starts, the controller reads measurement rules one-by-one from a pattern table. For each controller the scanning sequence includes 16 different rules at most, before repeating itself.

The 8-bit item (the pattern table register) is composed of three fields that contain channel, resolution and attenuation information, as shown in Table 31.3-3.

**Table Caption:**

- **Table 31.3-3. Fields of the Pattern Table Register**
  
  - ch_sel[3:0] | bit_width[1:0] | atten[1:0]
  - channel to be scanned | resolution | attenuation

**Footer Information:**

Espressif Systems
744 ESP32 TRM (Version 5.6)
Submit Documentation Feedback