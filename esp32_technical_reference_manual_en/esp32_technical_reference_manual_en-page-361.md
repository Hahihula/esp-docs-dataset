**Chapter Title:**
Chapter 20 SPI Controller (SPI)

**Figure Caption and Description:**
- **Figure 20.4-1. GP-SPI Slave Data Output:** A diagram showing the data output for a GP-SPI slave, with labels indicating CLK, MISO, t_spi, t_v, and t_pre.

**Body Text:**
To conclude, if signals do not pass through GPIO matrix, the SPI slave clock frequency is up to f_{app}/8; if signals pass through GPIO matrix, the SPI slave clock frequency is up to f_{app}/12. Note that (t_spi/2-t_pre) represents data output hold time for SPI slave in mode0 and mode2.

**Subsection Title:**
20.5 Parallel QSPI

**Body Text:**
ESP32 SPI controllers support SPI bus memory devices (such as flash and SRAM). The hardware connection between the SPI pins and the memories is shown by Figure 20.5-1.

**Figure Caption for Diagrams in Subsection:**
- **Figure 20.5-1. Parallel QSPI:** A diagram showing a parallel QSPI configuration with labels indicating Master (with connections to D, Q, WP, HD, CLK, CS0) and Slave (with connections labeled SI, SO, WP, HOLD, SCK, CE).

**Subsection Title:**
20.5.1 Communication Format of Parallel QSPI

**Body Text:**
To support communication with special slave devices, ESP32 QSPI implements a specifically designed communication protocol. The communication format of ESP32 QSPI master is the same as that of GP-SPI four-line half-duplex communication, except that in address phase and data phase, software can configure registers to enable two-line or four-line transmission. Figure 20.5-2 shows a QSPI communication mode with four-line transmission in address phase and data phase.

**Footer:**
Espressif Systems
361 ESP32 TRM (Version 5.6)
Submit Documentation Feedback