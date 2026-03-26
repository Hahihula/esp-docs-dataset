

```markdown
## 49.4 Functional Description

### 49.4.1 Controller Core and Interfaces

![Figure 49.4-1. OTG_HS System Architecture](image_path)

OTG_HS uses the same controller core as OTG_FS, i.e., USB Controller Core. The controller core has the following interfaces, see Figure 49.4-1:

*   **CPU Interface**
    Provides the CPU with read/write access to the controller core’s various registers and FIFOs. This interface is internally implemented as an AHB slave interface. The way to access the FIFOs through the CPU interface is called Slave mode.

*   **DMA Interface**
    Provides the controller core’s internal DMA with read/write access to system memory, e.g., fetching and writing data payloads in DMA mode. This interface is internally implemented as an AHB master interface.

*   **USB 2.0 Interface (USB 2.0 HS PHY)**
    This interface is used to connect the controller core to a USB 2.0 UTMI serial transceiver. With this serial transceiver, OTG_HS is able to support High-Speed data rate and Full-Speed data rate.

*   **Data FIFO Interface**
    The multiple FIFOs used by the controller core are not actually located within the controller core itself, but on the Single-Port RAM (SPRAM). FIFOs are dynamically sized, thus are allocated at run-time in the SPRAM. When the CPU, DMA, or the controller core attempts to read/write to FIFOs, those accesses are routed through the data FIFO RAM interface.

### 49.4.2 Memory Layout

Figure 49.4-2 illustrates the memory layout of the registers which are used to configure and control the USB Controller Core.
```