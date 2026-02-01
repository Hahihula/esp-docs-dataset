Title: Table 2-9. Peripheral Pin Assignment

The image contains a detailed table with multiple columns and rows, listing various pin assignments for different peripherals on an ESP32-S3 chip.

### Columns:
1. **Pin No**
2. **Pin Name**
3. **USB Serial/TXD** (Full-speed USB OTG)
4. **ADC0**
5. **ADC1**
6. **ADC2**
7. **Touch Sensor**
8. **LIRTO**
9. **UART0**
10. **SPI0/1 (recommended) / SPI2 (alternative)**
11. **PWR2 (recommended) / PWR2 (alternative)**
12. **TWI**
13. **LED PWM**
14. **I2S**
15. **LCD and Camera SPS**
16. **SD/MMC**
17. **MCPWM**
18. **RMT**

### Rows:
Each row corresponds to a specific pin on the ESP32-S3 chip, with various assignments listed under each column.

### Notes at Bottom of Page (small text):
- "For USB Serial/TXD and USB OTG use USB_D_ and USB_D_ when an internal PHT is used. For external PHTs or when configuring the USB_SERIAL_TXD, TXD0, PINS bit according to ESP32-S3 Technical Reference Manual."
- "Use Pin Selection: Signals of UART0, UART1, SPI0/1, and SPI2 interfaces can be mapped to any GPIO pins through the GPIO Matrix. Regardless of whether they are directly routed via read pins or via IO MUX."

### Additional Information:
- The document is labeled as a datasheet for ESP32-S3 Series.
- There's an instruction on how to select PHT, and references back to other sections in the technical reference manual.

The table provides specific pin assignments that can be used by developers when interfacing with various peripherals using the ESP32-S3 chip.