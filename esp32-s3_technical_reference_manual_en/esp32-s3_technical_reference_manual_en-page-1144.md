**Title: Chapter 30 SPI Controller (SPI)**

---

### Figure Caption:
Figure 30.7-2, SPI Clock Mode 1 or 3

### Text Content:

#### Description of the figure and its components in text format with explanations for each mode described below.

##### Modes Explanation:
- **Mode 0:** CPOL = 0, CPHA = 0; SCK is on when the SPI is in idle state; data is changed on the negative edge of SCK and sampled on the positive edge. The first data is shifted out before the first negative edge of SCK.
  
- **Mode 1:** CPOL = 0, CPHA = 1; SCK is off when the SPI is in idle state; data is changed on the positive edge of SCK and sampled on the negative edge.

- **Mode 2:** CPOL = 1, CPHA = 0; SCK is 1 when the SPI is in idle state; data is changed on the positive edge of SCK and sampled on the negative edge. The first data is shifted out before the first positive edge of SCK.
  
- **Mode 3:** CPOL = 1, CPHA = 1; SCK is off when the SPI is in idle state; data is changed on the negative edge of SCK and sampled on the positive edge.

#### Additional Information:
The four clock modes (0 ~ 3) are supported in GP-SPI master mode. The polarity and phase of GP-SPI clock control by bit `SPI_CK_IDLE_EDGE` in register `SPI_MISC_REG` and the bit `SPI_CK_OUT_EDGE` in register `SPI_USER_REG`. The register configuration for SPI clock modes (0 ~ 3) is provided in Table 30.7-1, which can be changed according to the path delay in application.

---

### Section Title:
**30.7.2 Clock Control in Master Mode**

### Text Content:

The four clock modes supported are controlled by specific bits as mentioned above and their configurations for different modes (Mode O ~ 3) is provided below table format, which can be adjusted based on the path delay requirements.

---

### Table Title:
**Table 30.7-1: Clock Phase and Polarity Configuration in Master Mode**

| Control Bit       | Mode 0   | Mode 1    | Mode 2     | Mode 3      |
|--------------------|----------|-----------|------------|-------------|
| `SPI_CK_IDLE_EDGE`| 0        | 0         | 1          | 1           |
| `SPI_CK_OUT_EDGE` | 0        | 1         | 1          | 0           |

---

### Footer:
Espressif Systems  
Page number: 1144  
Document version (Version 1.7)  

**Submit Documentation Feedback**

--- 

*Note: The diagram in the image is not described as it contains a complex waveform and timing chart which would be difficult to transcribe accurately without potentially losing context or detail.*