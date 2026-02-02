**Chapter Title:**
Chapter 27 SD/MMC Host Controller (SDHOST)

**Section Header:**
Register 27.1. CTRL_REG (0x0000)

**Body Text with Subsections and Descriptions:**

Continued from the previous page...

- **READ_WAIT**: For sending read-wait to SDIO cards.
  - Access Mode(s): Read/Write

- **INT_ENABLE**: Global interrupt enable/disable bit:
  - Value Options: 0: Disable; 1: Enable
  - Access Mode(s): Read/Write
  
- **DMA_RESET**: To reset DMA interface, firmware should set bit to 1. This bit is auto-cleared after two AHB clocks.
  - Access Mode(s): Read/Write

- **FIFO_RESET**: To reset FIFO, firmware should set bit to 1. This bit is auto-cleared after completion of reset operation:
  - Note: FIFO pointers will be out of reset after 2 cycles of system clocks in addition to synchronization delay (2 cycles of card clock), after the fifo_reset is cleared.
  - Access Mode(s): Read/Write

- **CONTROLLER_RESET**: To reset controller, firmware should set this bit. This bit is auto-cleared after two AHB and two cclk in clock cycles:
  - Access Mode(s): Read/Write

**Diagram Description:**
- The diagram shows a register layout with labels for different registers (CLK_DIVIDER3 to CLK_DIVIDERO) along the x-axis, each labeled as "0x000" or similar. There are also values associated at specific positions on these axes.

**Section Header:**
Register 27.2. CLKDIV_REG (0x0008)

**Body Text with Descriptions for Each Register:**

- **CLK_DIVIDER3**: Clock divider-3 value.
  - Description of clock division factor and its implications:
    - For example, a value of 1 means divide by \(2^*1 = 2\), a value of 0xFF means divide by \(2^*255 = 510\).
    - In MMC-Ver3.3-only mode: these bits are not implemented because only one clock divider is supported.
  - Access Mode(s): Read/Write

- **CLK_DIVIDER2**: Clock divider-2 value.
  - Description of clock division factor and its implications:
    - For example, a value of 1 means divide by \(2^*1 = 2\), a value of 0xFF means divide by \(2^*255 = 510\).
    - In MMC-Ver3.3-only mode: these bits are not implemented because only one clock divider is supported.
  - Access Mode(s): Read/Write

- **CLK_DIVIDER1**: Clock divider-1 value.
  - Description of clock division factor and its implications:
    - For example, a value of 1 means divide by \(2^*1 = 2\), a value of 0xFF means divide by \(2^*255 = 510\).
    - In MMC-Ver3.3-only mode: these bits are not implemented because only one clock divider is supported.
  - Access Mode(s): Read/Write

- **CLK_DIVIDERO**: Clock divider-0 value.
  - Description of clock division factor and its implications:
    - For example, a value of 1 means divide by \(2^*1 = 2\), a value of 0xFF means divide by \(2^*255 = 510\).
    - In MMC-Ver3.3-only mode: these bits are not implemented because only one clock divider is supported.
  - Access Mode(s): Read/Write

**Footer Information:**
Espressif Systems
Page Number: 612
Document Title: ESP32 TRM (Version 5.6)
Link Texts:
- Submit Documentation Feedback