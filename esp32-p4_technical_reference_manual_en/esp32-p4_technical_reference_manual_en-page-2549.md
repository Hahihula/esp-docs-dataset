

```markdown
## 50.4 Functional Description

### 50.4.1 Controller Core and Interfaces

**Figure 50.4-1. OTG_FS System Architecture**

The core part of the OTG_FS peripheral is the USB Controller Core. The controller core has the following interfaces, see Figure 50.4-1:

*   **CPU Interface**
    Provides the CPU with read/write access to the controller core’s various registers and FIFOs. This interface is internally implemented as an AHB slave interface. The way to access the FIFOs through the CPU interface is called Slave mode.

*   **APB Interface**
    Allows the CPU to control the USB controller core via the USB external controller.

*   **DMA Interface**
    Provides the controller core’s internal DMA with read/write access to system memory, e.g., fetching and writing data payloads in DMA mode. This interface is internally implemented as an AHB master interface.

*   **USB 2.0 Full-Speed Interface**
    ESP32-P4 has two full-speed transceivers. This interface is used to connect the controller core to one of USB 2.0 full-speed serial transceivers. Aside from USB OTG, ESP32-P4 also includes a USB Serial/JTAG controller, see Chapter 51USB Serial/JTAG Controller (USB_SERIAL_JTAG). These two USB controllers can utilize the integrated internal transceivers by time-division multiplexing. In the following sections, GPIO24 and GPIO25 are referred to as FS_PHY1, while GPIO26 and GPIO27 as FS_PHY2.
    By default FS_PHY1 connects to USB Serial/JTAG controller and FS_PHY2 to OTG_FS. The connection is configurable via eFuse settings:
        - 0: FS_PHY1 is connected to USB Serial/JTAG controller, while FS_PHY2 to OTG_FS.
        - 1: FS_PHY2 is connected to USB Serial/JTAG controller, while FS_PHY1 to OTG_FS.

*   **USB External Controller**
    The USB External Controller is primarily used to control the routing of the USB 2.0 full-speed serial interface to the internal registers, thus allowing the CPU to perform query operations, etc. The External Controller can also enable a power saving mode by gating the controller core’s clock, i.e., AHB clock, or
```