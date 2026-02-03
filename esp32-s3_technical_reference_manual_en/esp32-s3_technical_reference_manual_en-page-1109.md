**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**GoBack Link:** GoBack

**Section Heading and Subheading with Diagrams:**

- **Subsection Header**: 
  - Able to communicate with SPI devices, such as a sensor, a screen controller, as well as a flash or RAM chip.

- **Subsection Title**:  
  **30.4 Architectural Overview**
  
  *Diagram Description*: Figure shows an overview of the SPI module architecture including components like CPU, ICache, DCache, GDMA, Bridge, APB, Arbiters (SPI0 and SPI1), FSP1, GPIO Matrix, PAD, MUX.

- **Subsection Title**: 
  - **30.4.1 SPI Module Overview**

**Body Text:**
Figure 30.4-1 shows an overview of the SPI module. GP-SPI2 and GP-SPI3 exchange data with SPI devices in the following ways:
- CPU-controlled transfer: CPU ↔ GP-SPI2 (GP-SPI3) ↔ SPI devices
- DMA-controlled transfer: DMA ↔ GP-SPI2 (GP-SPI3) ↔ SPI devices

The signals for GP-SPI2 and GP-SPI3 are prefixed with “FSPI” (Fast SPI) and “SPI3”, respectively. FSPI bus signals are routed to GPIO pins via either GPIO matrix or IO MUX, while SPI3 bus signals are routed to GPIO pins via GPIO matrix only.

For more information:
- See Chapter 6: IO MUX and GPIO Matrix (GPIO, IO MUX).

The functionalities of GP-SPI2 and GP-SPI3 are nearly the same as those of GP-SPI2. GP-SPI2’s functionalities described in Section **30.5**.
- The differences between GP-SPI2 and GP-SPI3 will be discussed further.

**Subsection Title**: 
  - **30.5 Functional Description**

**Subsection Subtitle:**
  - Data Modes

**Body Text for Subsection on Data Modes:**  
GP-SPI can be configured as either a master or a slave to communicate with other SPI devices in the following data modes, see Table *30.5-1*. As a GP-SPI master, the data modes listed in this table are defined in Section **30.5.8**; as a GP-SPI slave, the data modes listed in this table are defined in Section 30.5.9.

**Table Title**: 
  - Table *30.5-1*. Data Modes Supported by GP-SPI2 and GP-SPI3

| Supported Mode | CMD Phase | Address Phase | Data Phase | GP-SPI2 | GP-SPI3 |
|-----------------|-----------|---------------|------------|---------|---------|
| 1-bit SPI       | 1-bit     | 1-bit         | 1-bit      | Y       | Y       |
| Dual SPI        | 1-bit     | 1-bit         | 2-bit      | Y       | Y       |
| Dual I/O Read   | 1-bit     | 2-bit         | -          | Y       | N       |

**Footer Information:**
- Espressif Systems
- Document Version (Version 1.7)
- Page Number and Submission Link:
  - ESP32-S3 TRM, page number not specified.
  - Submit Documentation Feedback