**Chapter Title:**
Chapter 27 SD/MMC Host Controller (SDHOST)

**Section Heading:**
27.3 SD/MMC External Interface Signals

**Body Text:**
The primary external interface signals, which enable the SD/MMC controller to communicate with an external device, are clock (clk), command (cmd) and data signals. Additional signals include the card interrupt, card detect, and write-protect signals. The direction of each signal is shown in Figure 27.3-1. The direction and description of each pin are listed in Table 27.3-1.

**Figure Caption:**
Figure 27.3-1. SD/MMC Controller External Interface Signals

**Table Title:**
Table 27.3-1. SD/MMC Signal Description

| Pin       | Direction | Description                                    |
|-----------|-----------|------------------------------------------------|
| cclk_out  | Output    | Clock signals for slave device                  |
| ccmd      | Duplex   | Duplex command/respons response lines          |
| cdata     | Duplex   | Duplex data read/write lines                   |
| card_detect_n | Input  | Card detection input line                       |
| card_write_prt | Input  | Card write protection status input              |

**Subsection Heading:**
27.4 Functional Description

**Sub-subsection Title and Body Text:**
27.4.1 SD/MMC Host Controller Architecture
The SD/MMC host controller consists of two main functional blocks, as shown in Figure 27.4-1:
- Bus Interface Unit (BIU): It provides APB interfaces for registers, data read and write operation by FIFO and DMA.
- Card Interface Unit (CIU): It handles external memory card interface protocols. It also provides clock control.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Page Number:** 598 ESP32 TRM (Version 5.6)