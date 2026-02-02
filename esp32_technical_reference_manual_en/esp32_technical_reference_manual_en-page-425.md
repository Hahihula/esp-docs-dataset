**Chapter Title:**
Chapter 22 I2S Controller (I2S)

**Section Header:**
GoBack

**Body Text with Table and Diagrams Description**

1. **Table Description:** 
   - The table is labeled "Table 22.4-5. Upsampling Rate Configuration".
   - It has columns for `f_pcm (KHz)`, `I2S_TX_PDM_FP`, `I2S_TX_PDM_FS`, and `f_pdm (KHz)`.
   - Values in the table are as follows:
     - 48 KHz: I2S_TX_PDM_FP = 960, I2S_TX_PDM_FS = 480
     - 44.1 KHz: No data provided for f_pdm (KHz)
     - 32 KHz: I2S_TX_PDM_FP = 960, I2S_TX_PDM_FS = 320
     - 24 KHz: I2S_TX_PDM_FP = 960, I2S_TX_PDM_FS = 240
     - 16 KHz: No data provided for f_pdm (KHz)
     - 8 KHz: No data provided

   **Explanation of Table Content:** 
   The text explains that the `I2S_TX_PDM_SINC_OS2` bit in I2S_PDM_CONF_REG is related to upsampling rate. It provides a formula for calculating this value based on different configurations.

2. **Text Explanation:**
   - "The I2S_TX_PDM_SINC_OS2 bit of I2S_PDM_CONF_REG is the upsampling rate of the Filter group0."
   - The specific configuration bits are listed as `I2S_TX_PDM_FP`, `I2S_TX_PDM_FS`.

3. **Figure Description:**
   Figure 22.4-8 shows "I2S PDM Sends Signal" with a block diagram labeled I2SOO WS_out and Data_out[23].

4. **Additional Text Explanation:** 
   - Describes the configuration bits `I2S_TX_PDMSigmaDelta_IN_SHIFT`, `I2S_TX_PDM_SINC_IN_SHIFT`, `I2S_TX_PDM_LP_IN_SHIFT`, and `I2S_TX_PDM_HP_IN_SHIFT` in relation to adjusting signal sizes for filter modules.

5. **Second Figure Description:**
   - "Figure 22.4-9, PDM Receives Signal" shows a block diagram labeled I2SO1 WS_out and Data_in[15].

6. **Additional Text Explanation:** 
   - Describes the configuration bits `I2S_RX_PDM_EN` bit in relation to using receiving modules.
   - Explains that filter group 1 is used for downsampling PDM signals, with a reference register I2S_PDM_CONF_REG.

**Footer:**
- "Espressif Systems"
- Page number and document version information:
  - Document page count or section identifier (425)
  - ESP32 TRM (Version 5.6)

This structured description captures the content, layout, headings, tables, diagrams, text explanations as presented in the image provided for Chapter 22 of an I2S Controller document by Espressif Systems.