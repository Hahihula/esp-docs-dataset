

```markdown
Figure 28.5-8 indicates GP-SPI2 Quad I/O Read sequence according to standard flash specification. Other GP-SPI2 command sequences are implemented in accordance with the requirements of SPI slaves.

Figure 28.5-8. SPI Quad I/O Read Command Sequence Sent by GP-SPI2 to Flash

28.5.8.5 DMA-Controlled Configurable Segmented Transfer

Note:
Note that there is no separate section on how to configure a single transfer as master, since the CONF state of a configurable segmented transfer can be skipped to implement a single transfer.

Introduction

When GP-SPI2 works as a master, it provides a feature named configurable segmented transfer controlled by DMA.

A DMA-controlled transfer as master can be
* a single transfer, consisting of only one transaction;
* or a configurable segmented transfer, consisting of several transactions (segments).

In a configurable segmented transfer, the registers of each single transaction (segment) are configurable. This feature enables GP-SPI2 to do as many transactions (segments) as configured after such transfer is triggered once by the CPU. Figure 28.5-9 shows how this feature works.

Figure 28.5-9. Configurable Segmented Transfer as Master

As shown in Figure 28.5-9, the registers for one transaction (segment n) can be reconfigured by GP-SPI2
```