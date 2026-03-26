

```markdown
Chapter 43 SPI Controller (SPI)                                                                 GoBack


Figure 43.5-7. Connection of GP-SPI2 to Flash and External RAM in 4-bit Mode

Master
GP-SPI2
SPI2D
SPI2Q
SPI2WP
SPI2HD
SPI2CLK
SPI2CS0

Slave (Flash)
SI
SO
WP
FLASH
HOLD
SCK
CE

Slave (SRAM)
SI
SO
WP
SRAM
HOLD
SCK
CE


Figure 43.5-8 indicates GP-SPI2 Quad I/O Read sequence according to standard flash specification. Other GP-SPI2 command sequences are implemented in accordance with the requirements of SPI slaves.


SPI2CLK
SPI2D   [0,1,2,3,4,5,6,7]
SPI2Q    4 0 4 0 4 0
SPI2WP   5 1 5 1 5 1
SPI2HD   6 2 6 2 6 2

Command phase | Address phase | Dummy phase | Data phase


Figure 43.5-8. SPI Quad I/O Read Command Sequence Sent by GP-SPI2 to Flash



43.5.9.5 DMA-Controlled Configurable Segmented Transfer

Note:
* LP-SPI and GP-SPI3 do not support DMA-controlled configurable segmented transfer.
* Note that there is no separate section on how to configure a single transfer as master, since the CONF state of a configurable segmented transfer can be skipped to implement a single transfer.



Introduction

When GP-SPI2 works as a master, it provides a feature named configurable segmented transfer controlled by DMA.

A DMA-controlled transfer as master can be:
* a single transfer, consisting of only one transaction;
* or a configurable segmented transfer, consisting of several transactions (segments).



Espressif Systems    2224
Submit Documentation Feedback      ESP32-P4 TRM PRELIMINARY
```