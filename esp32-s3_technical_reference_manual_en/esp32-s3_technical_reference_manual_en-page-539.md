**Chapter Title:**
Chapter 9

**Section Heading:**
Interrupt Matrix (INTERRUPT)

**Subsection 1: Overview**

The interrupt matrix embedded in ESP32-S3 independently allocates peripheral interrupt sources to the two CPUs’ peripheral interrupts, to timely inform CPU0 or CPU1 to process the interrupts once the interrupt signals are generated.

Peripheral interrupt sources must be routed to CPU0/CPU1 peripheral interrupts via this interrupt matrix due to the following considerations:

- ESP32-S3 has 99 peripheral interrupt sources. To map them to 32 CPU0 interrupts or 32 CPU1 interrupts, this matrix is needed.
- Through this matrix, one peripheral interrupt source can be mapped to multiple CPU0 interrupts or CPU1 interrupts according to application requirements.

**Subsection 2: Features**

Accept 99 peripheral interrupt sources as input

Generate 26 peripheral interrupts to CPU0 and 26 peripheral interrupts to CPU1 as output. Note that the remaining six CPU0 interrupts and six CPU1 interrupts are internal interrupts.

Support to disable CPU non-maskable interrupt (NMI) sources

Support to query current interrupt status of peripheral interrupt sources

**Figure Caption:**
Figure 9.2-1 shows the structure of the interrupt matrix.

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback