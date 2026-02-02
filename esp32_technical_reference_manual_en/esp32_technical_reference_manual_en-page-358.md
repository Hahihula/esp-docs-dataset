**Title: Chapter 20 SPI Controller (SPI)**

**Section Title:** GP-SPI Data Buffer  
**Subsection Number and Name:** 20.3.4 GP-SPI Data Buffer  

**Figure Caption:** Figure 20.3-2. SPI Data Buffer

**Body Text:**
ESP32 SPI has 16 x 32 bits of data buffer to buffer data send-and-receive operations. As is shown in Figure 20.3-2, received data is written from the low byte of SPI_WO_REG by default and the writing ends with SPI_W15_REG. If the data length is over 64 bytes, the extra part will be written from SPI_WO_REG.

Data buffer blocks SPI_WO_REG ~ SPI_W7_REG and SPI_W8_REG ~ SPI_W15_REG data correspond to the lower part and the higher part respectively. They can be used separately, and are controlled by the SPI_USR_MOSI._HIGHPART bit and the SPI_USR_MISO_HIGHPART bit in register SPI_USER_REG. For example, if SPI is configured as a master, when SPI_USR_MOSI_HIGHPART = 1, SPI_W8_REG ~ SPI_W15_REG are used as buffer for sending data; when SPI_USR_MISO_HIGHPART = 1, SPI_W8_REG ~ SPI_W15_REG are used as buffer for receiving data. If SPI acts as a slave, when SPI_USR_MOSI_HIGHPART = 1,

SPI_W8_REG ~ SPI_W15_REG are used as buffer for receiving data; when SPI_USR_MISO_HIGHPART = 1,
SPI_W8_REG ~ SPI_W15_REG are used as buffer for sending data.

**Subsection Number and Name:**  
20.4 GP-SPI Clock Control

**Body Text:**
The maximum output clock frequency of ESP32 GP-SPI master is f_{app}/2, and the maximum input clock frequency of the ESP32 GP-SPI slave is f_{app}/8. The master can derive other clock frequencies via frequency division.

f_{spi} = (SPI_CLKCNT_N+1)(SPI_CLKDIV_PRE+1)

**Body Text:**
SPI_CLKCNT_N and SPI_CLKDIV_PRE are two bits of register SPI CLOCK_REG (Please refer to 20.7 Register Description for details). SPI_CLKCNT_H = [SPI_CLKCNT_N+1-1], SPI_CLKCNT_N=SPI_CLKCNT_L. When the SPI_CLK_EQU_SYSCLK bit in register SPI_CLOCK_REG is set to 1, and the other bits are set to O, SPI output clock frequency is f_{app}. For other clock frequencies, SPI_CLK_EQU_SYSCLK needs to be O. In slave mode,
SPI_CLKCNT_N, SPI_CLKCNT_L, SPI_CLKCNT_H and SPI_CLKDIV_PRE should all be O.

**Subsection Number and Name:**  
20.4.1 GP-SPI Clock Polarity (CPOL) and Clock Phase (CPHA)

**Body Text:**
The clock polarity and clock phase of ESP32 SPI are controlled by SPI_CLK_IDLE_EDGE bit in register SPI_PIN_REG, SPI_CK_OUT EDGE bit and SPI_CK_I_EDGE bit in register SPI_USER_REG, as well as

**Footer:**  
Espressif Systems  
Page number 358  
Submit Documentation Feedback  

**Note:**
- The figure shows a table with the following structure:
  - Row labels (from top to bottom): 
    - SP1_W0_REG
    - SP1_W7_REG
    - SP1_W8_REG
    - SP1_W15_REG
  - Column headers from left to right:  
    - 31, Low, High

- The figure caption is "Figure 20.3-2. SPI Data Buffer".