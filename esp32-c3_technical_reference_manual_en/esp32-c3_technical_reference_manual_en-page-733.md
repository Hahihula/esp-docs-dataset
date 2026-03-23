

```markdown
Chapter 29 I2S Controller (I2S)  
GoBack  

- "B": signal function  
  - BCK  
  - WS  
  - SD  
- "C": signal direction  
  - "in": input signal into I2S module  
  - "out": output signal from I2S module  

Table 29.4-1 provides a detailed description of I2S signals.  

Table 29.4-1. I2S Signal Description  

| Signal          | Direction | Function                                                                 |
|-----------------|-----------|--------------------------------------------------------------------------|
| I2SI_BCK_in     | Input     | In I2S slave mode, inputs BCK signal for RX unit.                       |
| I2SI_BCK_out    | Output    | In I2S master mode, outputs BCK signal for RX unit.                     |
| I2SI_WS_in      | Input     | In I2S slave mode, inputs WS signal for RX unit.                        |
| I2SI_WS_out     | Output    | In I2S master mode, outputs WS signal for RX unit.                      |
| I2SI_Data_in    | Input     | Works as the serial input data bus for I2S RX unit.                     |
| I2SO_Data_out   | Output    | Works as the serial output data bus for I2S TX unit.                    |
| I2SO_BCK_in     | Input     | In I2S slave mode, inputs BCK signal for TX unit.                       |
| I2SO_BCK_out    | Output    | In I2S master mode, outputs BCK signal for TX unit.                     |
| I2SO_WS_in      | Input     | In I2S slave mode, inputs WS signal for TX unit.                        |
| I2SO_WS_out     | Output    | In I2S master mode, outputs WS signal for TX unit.                      |
| I2S_MCLK_in     | Input     | In I2S slave mode, works as a clock source from the external mas-ter.   |
| I2S_MCLK_out    | Output    | In I2S master mode, works as a clock source for the external slave.     |

Note:  
Any required signals of I2S must be mapped to the chip’s pins via GPIO matrix, see Chapter 5 IO MUX and GPIO Matrix (GPIO, IO MUX).  

## 29.5 Supported Audio Standards  

ESP32-C3 I2S supports multiple audio standards, including TDM Philips standard, TDM MSB alignment standard, TDM PCM standard, and PDM standard. Select the needed standard by configuring the following bits:  

- **I2S_TX/RX_TDM_EN**  
  - 0: disable TDM mode.  
  - 1: enable TDM mode.  
- **I2S_TX/RX_PDM_EN**  


Espressif Systems  
733  
ESP32-C3 TRM (Version 1.3)  

Submit Documentation Feedback
```