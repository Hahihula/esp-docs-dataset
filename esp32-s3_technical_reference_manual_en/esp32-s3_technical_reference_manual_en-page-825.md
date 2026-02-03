**Chapter Title:**
Chapter 17 System Registers (SYSTEM)

**Section Heading and Subheading with Content:**

- **Subsection:** SYSTEM_RTC_FASTMEM_CRC_REG : configures the CRC check value.
  
- **Title:** 17.3.5 Peripheral Clock Gating and Reset Registers

- **Body Text:**
The following registers are used for controlling the clock gating and reset of different peripherals. Details can be seen in Table 17.3-2.

**List with Code Names (in blue):**
- SYSTEM_CACHE_CONTROL_REG
- SYSTEM_EDMA_CTRL_REG
- SYSTEM_PERIP_CLK_EN0_REG
- SYSTEM_PERIP_RST_EN0_REG
- SYSTEM_PERIP_CLK_EN1_REG
- SYSTEM_PERIP_RST_EN1_REG

**Body Text:**
ESP32-S3 features low power consumption. This is why some peripheral clocks are gated (disabled) by default. Before using any of these peripherals, it is mandatory to enable the clock for the given peripheral and release the peripheral from reset state. For details, see the table below:

**Table Title:** Table 17.3-2. Peripheral Clock Gating and Reset Bits

| Peripheral | Clock Enabling Bit^1 | Reset Controlling Bit^2 |
|------------|-----------------------|-------------------------|
| EDMA Ctrl  |                      | SYSTEM_EDMA_CTRL_REG    |
|            |                       |                        |
|            |                       |                        |
|            |                       |                        |
|            |                       |                        |
|            |                       |                        |
|            |                       |                        |
|            |                       |                        |

**Table with Columns:**
- **Peripheral**
  - EDMA
  - CACHE Ctrl
  - DCACHE
  - ICACHE
  - Timer Group0
  - Timer Group1
  - System Timer
  - UART0
  - UART1
  - UART MEM
  - SPI0, SPI1
  - SPI2
  - SPI3
  - I2C0
  - I2C1
  - I2S0
  - I2S1
  - TWAI Controller
  - UHCI0
  - USB
  - RMT
  - PCNT

- **Clock Enabling Bit^1**
  - SYSTEM_EDMA_CLK_ON
  - SYSTEM_CACHE_CONTROL_REG
  - SYSTEM_DCACHE_CLK_ON
  - SYSTEM_ICACHE_CLK_ON
  - SYSTEM_TIMERGROUP1_CLK_EN
  - SYSTEM_SYSTEMIMER_CLK_EN
  - SYSTEM_UART_CLK_EN
  - SYSTEM_UART1_CLK_EN
  - SYSTEM_UART_MEM_CLK_EN
  - SYSTEM_SPI01_CLK_EN
  - SYSTEM_SPI2_CLK_EN
  - SYSTEM_SPI3_CLK_EN
  - SYSTEM_I2C_EXT_CLK_EN
  - SYSTEM_I2SO_CLK_EN
  - SYSTEM_I2S1_CLK_EN
  - SYSTEM_CAN_CLK_EN
  - SYSTEM_UHCI0_CLK_EN
  - SYSTEM_USB_CLK_EN
  - SYSTEM_RMT_CLK_EN
  - SYSTEM_PCNT_CLK_EN

- **Reset Controlling Bit^2**
  - SYSTEM_EDMA_RESET
  - SYSTEM_CACHE_CONTROL_REG
  - SYSTEM_DCACHE_RESET
  - SYSTEM_ICACHE_RESET
  - SYSTEM_TIMERGROUP1_RST
  - SYSTEM_SYSTEMER_RST
  - SYSTEM_UART_RST
  - SYSTEM_UART1_RST
  - SYSTEM_UART_MEM_RST
  - SYSTEM_SPI01_RST
  - SYSTEM_SPI2_RST
  - SYSTEM_SPI3_RST
  - SYSTEM_I2C_EXT_RST
  - SYSTEM_I2SO_RST
  - SYSTEM_I2S1_RST
  - SYSTEM_CAN_RST
  - SYSTEM_UHCI_RST
  - SYSTEM_USB_RST
  - SYSTEM_RMT_RST
  - SYSTEM_PCNT_RST

**Footer:**
Espressif Systems  
Submit Documentation Feedback  
ESP32-S3 TRM (Version 1.7) Page number at the bottom center is "825".