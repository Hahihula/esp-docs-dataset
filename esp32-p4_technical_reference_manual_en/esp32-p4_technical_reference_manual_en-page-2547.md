

```markdown
Chapter 50

USB 2.0 Full-Speed OTG

50.1 Overview

The ESP32-P4 features a USB 2.0 Full-Speed On-The-Go peripheral (henceforth referred to as OTG_FS) along with integrated transceivers. This OTG_FS conforms to USB 2.0 specification, OTG Revision 1.3, and OTG Revision 2.0 specifications, OTG_FS can operate as either a USB Host or Device and supports 12 Mbit/s full-speed (FS) and 1.5 Mbit/s low-speed (LS) data rates of the USB 2.0 specification. The Host Negotiation Protocol (HNP) and the Session Request Protocol (SRP) are also supported.

50.2 Glossary

The following abbreviations and terms are used in this chapter.

| Term | Definition |
|------|------------|
| **Host** | The host computer system where the USB Host Controller is installed. This includes the host hardware platform (CPU, bus, etc.) and the operating system in use. |
| **Device** | A logical or physical entity that performs a function. The actual entity described depends on the context of the reference. At the lowest level, device may refer to a single hardware component, as in a memory device. At a higher level, it may refer to a collection of hardware components that perform a particular function, such as a USB interface device. At an even higher level, device may refer to the function performed by an entity attached to the USB; for example, a data/FAX modem device. When used as a non-specific reference, a USB device is either a hub or a function. |
| **Full-speed** | USB operation at 12 Mbit/s. |
| **Low-speed** | USB operation at 1.5 Mbit/s. |
| **Host Negotiation Protocol (HNP)** | Allows the host function to be transferred between two directly connected OTG devices and eliminates the need for a user to switch the cable connections in order to allow a change in control of communications between the devices. |
| **Session Request Protocol (SRP)** | Allows a B-device to request the A-device to turn on the power supply to the USB interface (VBUS) and start a session. |
| **Endpoint** | A uniquely addressable portion of a USB device that is the source or sink of information in a communication flow between the host and device. |
| **Scatter/Gather DMA mode** | Accesses discontinuous memory areas via DMA. |
```