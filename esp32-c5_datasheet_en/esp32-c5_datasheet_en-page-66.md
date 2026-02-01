**Title:**
5 Electrical Characteristics

**Subtitle and Body Texts with Structure Indicators (e.g., headings, tables):**

1. **Section Title:** 
   - Absolute Maximum Ratings
  
2. **Body Text under Section 5.1:**
   - "Stresses above those listed in Table 5-1 *Absolute Maximum Ratings* may cause permanent damage to the device. These are stress ratings only and normal operation of the device at these or any other conditions beyond those indicated in Section 5.2 Recommended Power Supply Characteristics is not implied. Exposure to absolute-maximum-rated conditions for extended periods may affect device reliability."

3. **Table Title:**
   - Table 5-1. Absolute Maximum Ratings

4. **Table Content (with headers and data):**
   - Parameter | Description | Min | Max | Unit
   - Input power pins¹ | Allowed input voltage | –0.3 V | 3.6 V |
   - T STORE | Storage temperature | –40 °C | 150 °C |

5. **Footnote under Table:**
   - "¹ For more information on input power pins, see Section 2.5.1 Power Pins."

6. **Section Title:** 
   - Recommended Power Supply Characteristics

7. **Body Text under Section 5.2:**
   - "For recommended ambient temperature, see Section 1 ESP32-C5 Series Information."
   
8. **Table Title:**
   - Table 5-2. Recommended Power Characteristics

9. **Table Content (with headers and data):**
   - Parameter | Description | Min | Typ | Max | Unit
   - VDDA1, VDDA2, VDDA3, VDDA4, VDDA5, VDDA6, VDDA7, VDDA8 | Recommended input voltage | 3.0 V | — | 3.6 V |
   - VDDPST1, VDDPST3 | Recommended input voltage | 3.0 V | 3.3 V | 3.6 V |
   - VDD_SPI (as input) | – | — | 3.3 V | 
   - VDDPST2²,³ | Recommended input voltage | 3.0 V | 3.3 V | 3.6 V |
   - I VDD | Cumulative input current | 0.6 A | — | 

10. **Footnotes under Table:**
    - "¹ See in conjunction with Section 2.5 Power Supply."
    - "² If VDDPST2 is used to power VDD_SPI (see Section 2.5.2 Power Scheme), the voltage drop on R_SPI should be accounted for."
    - "³ If writing to eFuses, the voltage on VDDPST2 should not exceed 3.3 V as the circuits responsible for burning eFuses are sensitive to higher voltages."

**Footer:**
- Espressif Systems
- Page number and document version information:
   - ESP32-C5 Series Datasheet v1.0, page 66.
- Link text (presumably a button or link): "Submit Documentation Feedback"