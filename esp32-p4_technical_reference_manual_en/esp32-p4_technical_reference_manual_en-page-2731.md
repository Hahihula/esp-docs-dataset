

```markdown
Chapter 54 SD/MMC Host Controller (SDHOST)

GoBack

* Card Interface Unit (CIU): handles external memory card interface protocols and provides clock control.

Figure 54.4-1. SDIO Host Block Diagram


54.4.1.1 Bus Interface Unit (BIU)

The BIU provides access to registers and RAM data through the Host Interface Unit (HIU). Additionally, it provides a method to access to memory data through a DMA interface. Figure 54.4-1 illustrates the internal components of the BIU.

The BIU provides the following functions:

* Host interface
* DMA interface
* Interrupt control
* Register access
* FIFO access
* Power-up/pull-up control and card detection

54.4.1.2 Card Interface Unit (CIU)

The CIU module implements the dedicated card slot specifications. Within the CIU, the command path control unit and data path control unit are used to interface with the command and data ports, respectively, of the SD/MMC/CE-ATA cards. The CIU also provides clock control. Figure 54.4-1 illustrates the internal structure of the CIU, which consists of the following primary functional blocks:

* Command path
* Data path
* SDIO interrupt control
* Clock control
* MUX (multiplexer) and De-MUX (de-multiplexer) unit

Espressif Systems    2731    ESP32-P4 TRM PRELIMINARY
Submit Documentation Feedback
```