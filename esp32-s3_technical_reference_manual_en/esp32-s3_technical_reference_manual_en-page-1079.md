**Title:**
Chapter 29 LCD and Camera Controller (LCD_CAM)

**Diagram Description:**
- Figure Caption: "Figure 29.3-1. LCD_CAM Block Diagram"
- The diagram shows the connections between various components such as PLL_F160M_CLK, RX_FIFO, TX_FIFO, CAM_CLK, CAM_H_SYNC, CAM_V_SYNC, etc.

**Subtitle and Section Title:**
29.3.2 Signal Description

**Table Caption:**
Table 29.3-1. Signal Description

**Table Content (with headers):**

| Operation Mode | Signal       | Direction | Function                                    |
|-----------------|-------------|-----------|---------------------------------------------|
|                  | CAM_PCLK    | Input     | Camera pixel clock signal                    |
|                  | CAM_V_SYNC  | Input     | Vertical synchronization signal (VSYNC)      |
| **Camera Slave RX Mode** | CAM_H_SYNC   | Input     | Horizontal synchronization signal (HSYNC)    |
|                   | CAM_H_ENABLE| Input     | Horizontal enable signal (DE)               |
|                   | CAM_Data_in[N:0]² | Input  | Camera parallel input data bus, 8-/16-bit supported |
|                  | CAM_PCLK    | Output    | Camera pixel clock input signal              |
| **Camera Master RX Mode** | CAM_M_CLK   | Output    | Camera master clock output signal            |
|                   | CAM_V_SYNC  | Input     | Vertical synchronization signal (VSYNC)      |
|                   | CAM_H_SYNC  | Input     | Horizontal synchronization signal (HSYNC)    |
|                   | CAM_H_ENABLE| Input     | Horizontal enable signal (DE)               |
|                   | CAM_Data_in[N:0]² | Input  | Camera parallel input data bus, 8-/16-bit supported |
|                  | LCD_PCLK   | Output    | LCD pixel clock signal                       |
| **LCD Master TX Mode** | LCD_H_SYNC  | Output    | Horizontal synchronization signal in RGB format|
|                   | LCD_V_SYNC  | Output    | Vertical synchronization signal in RGB mode  |
|                   | LCD_H_ENABLE| Output    | Horizontal enable signal (DE)               |
|                   | LCD_CD     | Output    | Command and data (CD) signal in I8080 format |
|                   | LCD_CS     | Output    | Chip select (CS) signal in I8080/MOTO6800 format|
|                  | LCD_Data_out[N:0]² | Output  | LCD parallel output data bus, 8-/16-bit supported |

**Footer Information:**
- Page number and document version information at the bottom of each page.
- "Espressif Systems" logo
- Document feedback link

(Note: The superscripted numbers [N:0], [2] refer to specific notes or references that are likely detailed elsewhere in the documentation.)