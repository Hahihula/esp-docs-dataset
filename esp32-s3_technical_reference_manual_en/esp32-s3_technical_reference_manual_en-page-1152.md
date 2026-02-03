**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**GoBack Link:** [GoBack](#)

---

### Table of Registers

| Name                          | Description                                                                                   | SPI2 Address       | SPI3 Address       | Access |
|-------------------------------|---------------------------------------------------------------------------------------------|--------------------|--------------------|--------|
| **SPI_CLK_GATE_REG**         | SPI module clock and register clock control                                                 | 0x00E8            | 0x00E8             | R/W    |
| **Timing registers**          |                                                                                               |                    |                    |        |
| **SPI_DIN_MODE_REG**         | SPI input delay mode configuration                                                          | 0x0024            | 0x0024             | R/W    |
| **SPI_DIN_NUM_REG**          | SPI input delay number configuration                                                        | 0x0028            | 0x0028             | R/W    |
| **SPI_DOUT_MODE_REG**        | SPI output delay mode configuration                                                         | 0x002C            | 0x002C             | R/W    |
| **Interrupt registers**      |                                                                                               |                    |                    |        |
| **SPI_DMA_INT_ENA_REG**      | SPI interrupt enable register                                                              | 0x0034            | 0x0034             | R/W    |
| **SPI_DMA_INT_CLR_REG**      | SPI interrupt clear register                                                               | 0x0038            | 0x0038             | WT     |
| **SPI_DMA_INT_RAW_REG**      | SPI interrupt raw register                                                                | 0x003C            | 0x003C             | R/W/TCC/SS|
| **SPI_DMA_INT_ST_REG**       | SPI interrupt status register                                                              | 0x0040            | 0x0040             | RO     |
| **SPI_DMA_INT_SET_REG**      | SPI interrupt software set register                                                        | 0x0044            | 0x0044             | WT     |
| **CPU-controlled data buffer**|                                                                                               |                    |                    |        |
| **SPI_WO_REG**               | SPI CPU-controlled buffer0                                                                | 0x0098            | 0x0098             | R/W/SS |
| **SPI_W1_REG**               | SPI CPU-controlled buffer1                                                                | 0x009C            | 0x009C             | R/W/SS |
| **SPI_W2_REG**               | SPI CPU-controlled buffer2                                                                | 0x00A0            | 0x00A0             | R/W/SS |
| **SPI_W3_REG**               | SPI CPU-controlled buffer3                                                                | 0x00A4            | 0x00A4             | R/W/SS |
| **SPI_W4_REG**               | SPI CPU-controlled buffer4                                                                | 0x00A8            | 0x00A8             | R/W/SS |
| **SPI_W5_REG**               | SPI CPU-controlled buffer5                                                                | 0x00AC            | 0x00AC             | R/W/SS |
| **SPI_W6_REG**               | SPI CPU-controlled buffer6                                                                | 0x00B0            | 0x00B0             | R/W/SS |
| **SPI_W7_REG**               | SPI CPU-controlled buffer7                                                                | 0x00B4            | 0x00B4             | R/W/SS |
| **SPI_W8_REG**               | SPI CPU-controlled buffer8                                                                | 0x00B8            | 0x00B8             | R/W/SS |
| **SPI_W9_REG**               | SPI CPU-controlled buffer9                                                                | 0x00BC            | 0x00BC             | R/W/SS |
| **SPI_W10_REG**              | SPI CPU-controlled buffer10                                                               | 0x00C0           | 0x00C0             | R/W/SS |
| **SPI_W11_REG**              | SPI CPU-controlled buffer11                                                               | 0x00C4           | 0x00C4             | R/W/SS |
| **SPI_W12_REG**              | SPI CPU-controlled buffer12                                                               | 0x00C8           | 0x00C8             | R/W/SS |
| **SPI_W13_REG**              | SPI CPU-controlled buffer13                                                               | 0x00CC           | 0x00CC             | R/W/SS |
| **SPI_W14_REG**              | SPI CPU-controlled buffer14                                                               | 0x00D0           | 0x00D0             | R/W/SS |
| **SPI_W15_REG**              | SPI CPU-controlled buffer15                                                               | 0x00D4           | 0x00D4             | R/W/SS |
| **Version register**         |                                                                                               |                    |                    |        |
| **SPI_DATE_REG**             | Version control                                                                            | 0x00F0            | 0x00F0             | R/W    |

---

### Section Title: 
30.12 Registers

### Body Text:
The addresses in this section are relative to SPI2/SPI3 base address provided in Table **4.3-3** in Chapter *4 System and Memory*.

---

**Footer Information:**  
Espressif Systems  
Page Number: 1152  
Document Title: ESP32-S3 TRM (Version 1.7)  

**Links:**
- Submit Documentation Feedback