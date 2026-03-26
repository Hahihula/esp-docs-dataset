

```markdown
Chapter 49 USB 2.0 High-Speed OTG

GoBack

Chapter 49

USB 2.0 High-Speed OTG

49.1 Overview

The ESP32-P4 chip features a USB 2.0 High-Speed On-The-Go peripheral (OTG_HS) with an integrated transceiver. This OTG_HS complies with the USB 2.0 specification, OTG Revision 1.3, and OTG Revision 2.0 specifications. The interface supports USB 2.0 High-Speed mode (480 Mbit/s), Full-Speed mode (12 Mbit/s), and Low-Speed mode (1.5 Mbit/s).

- When OTG_HS operates in High-Speed or Full-Speed modes, it can be configured as either a Host or a Device.
- When OTG_HS operates in Low-Speed mode, it can only be configured as a Host.

49.2 Glossary

The following abbreviations and terms are used in this chapter.

| Term                  | Definition                                                                 |
|-----------------------|-----------------------------------------------------------------------------|
| Host                  | The host computer system where the USB Host Controller is installed. This includes the host hardware platform (CPU, bus, etc.) and the operating system in use. |
| Device                | A logical or physical entity that performs a function. The actual entity described depends on the context of the reference. At the lowest level, device may refer to a single hardware component, as in a memory device. At a higher level, it may refer to a collection of hardware components that perform a particular function, such as a USB interface device. At an even higher level, device may refer to the function performed by an entity attached to the USB; for example, a data/FAX modem device. When used as a non-specific reference, a USB device is either a hub or a function. |
| High-speed            | USB operation at 480 Mbit/s.                                               |
| Full-speed            | USB operation at 12 Mbit/s.                                                |
| Low-speed             | USB operation at 1.5 Mbit/s.                                               |
| Endpoint              | A uniquely addressable portion of a USB device that is the source or sink of information in a communication flow between the host and device. |
| Scatter/Gather DMA mode | Accesses discontinuous memory areas via DMA.                              |
| Buffer DMA mode       | Accesses contiguous memory areas via DMA.                                  |
| Slave mode            | Accesses memory area through the CPU.                                     |
| RX FIFO               | Stores the received data.                                                  |

Espressif Systems          2535
Submit Documentation Feedback   ESP32-P4 TRM
PRELIMINARY
```