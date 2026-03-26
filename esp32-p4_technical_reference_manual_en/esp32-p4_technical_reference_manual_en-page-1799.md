

```markdown
| Operation Mode | Signal¹ | Direction | Function |
|----------------|---------|-----------|----------|
| Camera Slave RX Mode | CAM_PCLK | Input | Camera pixel clock signal |
|  | CAM_VSYNC | Input | Vertical synchronization signal (VSYNC)³ |
|  | CAM_HSYNC | Input | Horizontal synchronization signal (HSYNC)³ |
|  | CAM_DE | Input | Horizontal enable signal (DE)³ |
|  | CAM_Data_in[N:0]² | Input | Camera parallel input data bus, 8/16-bit modes supported |
| Camera Master RX Mode | CAM_PCLK | Input | Camera pixel clock input signal |
|  | CAM_CLK | Output | Camera master clock output signal |
|  | CAM_VSYNC | Input | Vertical synchronization signal³ |
|  | CAM_HSYNC | Input | Horizontal synchronization signal³ |
|  | CAM_DE | Input | Horizontal enable signal³ |
|  | CAM_Data_in[N:0]² | Input | Camera parallel input data bus, 8/16-bit modes supported |
| LCD Master TX Mode | LCD_PCLK | Output | LCD pixel clock signal |
|  | LCD_HSYNC | Output | Horizontal synchronization signal in RGB format |
|  | LCD_VSYNC | Output | Vertical synchronization signal in RGB format |
|  | LCD_DE | Output | Horizontal enable signal in RGB format |
|  | LCD_CD | Output | Command and data (CD) signal in I8080 format |
|  | LCD_CS | Output | Chip select (CS) signal in I8080/MOTO6800 format |
|  | LCD_Data_out[M:0]² | Output | LCD parallel output data bus, 8/16/24-bit modes supported |

---

¹ All the signals must be mapped to the chip’s pins via GPIO matrix. For more information, see Chapter 9 GPIO Matrix and IO MUX.
² For the input signals with 8 or 16-bit width, N = 7 or 15 respectively. For the output signals with 8, 16, or 24-bit width, M = 7, 15, or 23 respectively.
³ If LCD_CAM_CAM_VH_DE_MODE_EN is set, i.e., VSYNC + HSYNC mode is selected, then VSYNC, HSYNC, and DE signals control the data. In this case, users need to wire the three signal lines. If LCD_CAM_CAM_VH_DE_MODE_EN is cleared, i.e., DE mode is selected, then VSYNC and DE signals control the data. In this case, wiring HSYNC signal line is not a must. But in this case, the YUV-RGB conversion function of the Camera module is not available.
```

## 38.3.3 LCD_CAM Module Clocks

### 38.3.3.1 LCD Clock

The clocks used in the LCD module are generated from clock sources by the LCD_Clock Generator, see Figure 38.3-2. The clocks include:

*   Master clock: LCD_CLK, divided from the clock sources
*   Pixel clock: LCD_PCLK, divided from LCD_CLK