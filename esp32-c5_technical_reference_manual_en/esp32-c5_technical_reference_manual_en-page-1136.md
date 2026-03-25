

```markdown
Figure 33.5-8. SPI Quad I/O Read Command Sequence Sent by GP-SPI2 to Flash

33.5.9.5 DMA-Controlled Configurable Segmented Transfer

Note:
Users can simply skip the CONF state of a configurable segmented transfer to implement a single transfer, so there is no separate section on how to configure a single transfer as master.

Introduction

When GP-SPI2 works as a master, it provides a feature named configurable segmented transfer controlled by DMA.

A DMA-controlled transfer as master can be:

- a single transfer, consisting of only one transaction;
- or a configurable segmented transfer, consisting of several transactions (segments).

In a configurable segmented transfer, the registers of each single transaction (segment) are configurable. This feature enables GP-SPI2 to do as many transactions (segments) as configured after such transfer is triggered once by the CPU. Figure 33.5-9 shows how this feature works.

Figure 33.5-9. Configurable Segmented Transfer

As shown in Figure 33.5-9, the registers for one transaction (segment n) can be reconfigured by GP-SPI2 hardware according to the content in its Conf_bufn during the CONF state, before this segment starts.

It is recommended to provide separate GDMA CONF links and CONF buffers (Conf_bufi in Figure 33.5-9) for each CONF state. A GDMA TX link is used to connect all the CONF buffers and all TX data buffers (Tx_bufi in
```