**Chapter Title:**
Chapter 8

**Section Titles and Content:**

1. **Interrupt Matrix (INTERRUPT)**
   - Subsection "8.1 Overview"
     - The Interrupt Matrix embedded in the ESP32 independently allocates peripheral interrupt sources to the two CPUs’ peripheral interrupts. This configuration is made to be highly flexible in order to meet many different needs.

2. **Features** 
   - 8.2 Features
     - Accepts 71 peripheral interrupt sources as input.
     - Generates 26 peripheral interrupt sources per CPU as output (52 total).
     - CPU NMI Interrupt Mask.
     - Queries current interrupt status of peripheral interrupt sources.

3. **Functional Description**
   - Subsection "8.3 Functional Description"

**Figure:**
- Figure captioned “Interrupt Matrix Structure” with the figure number 8.2-1, showing a block diagram related to the structure described in section features.
  
**Footer Information:** 
- Page Number and Document Version:
  - Espressif Systems
  - ESP32 TRM (Version 5.6)
  - Submit Documentation Feedback

**Navigation Link:**
- GoBack