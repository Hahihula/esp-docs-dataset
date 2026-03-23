

```markdown
Figure 27.5-7. Connection of GP-SPI2 to Flash and External RAM in 4-bit Mode

Master
FSPID
FSPIQ
FSPIWP
FSPIHD
FSPICLK
FSPICS0

Slave (Flash)
SI
SO
WP
HOLD
SCK
CE

Slave (SRAM)
SI
SO
WP
HOLD
SCK
CE

GP-SPI2
FSPICS1

Figure 27.5-8 indicates GP-SPI2 Quad I/O Read sequence according to standard flash specification. Other GP-SPI2 command sequences are implemented in accordance with the requirements of SPI slaves.

Figure 27.5-8. SPI Quad I/O Read Command Sequence Sent by GP-SPI2 to Flash

Command phase
Address phase
Dummy phase
Data phase

0 1 2 3 4 5 6 7
4 0 4 0 4 0
5 1 5 1 5 1
6 2 6 2 6 2
7 3 7 3 7 3

27.5.8.5 DMA-Controlled Configurable Segmented Transfer

Note:
Note that there is no separate section on how to configure a single transfer in master mode, since the CONF state of a configurable segmented transfer can be skipped to implement a single transfer.

Introduction

When GP-SPI2 works as a master, it provides a feature named: configurable segmented transfer controlled by DMA.

A DMA-controlled transfer in master mode can be
- a single transfer, consisting of only one transaction;
- or a configurable segmented transfer, consisting of several transactions (segments).

In a configurable segmented transfer, the registers of its each single transaction (segment) are configurable.
```