

```markdown
Chapter 40
MIPI CSI

40.1 Introduction

The MIPI CSI module of ESP32-P4 provides a standard interface with camera modules for mobile devices, such as smartphones, tablets, and other portable electronics. It connects cameras to application processors in mobile devices, enabling high-speed data transfer and efficient communication between the camera and the host system.

ESP32-P4 MIPI CSI implements a MIPI RX D-PHY and a MIPI CSI-2 host controller. It provides one clock lane and two data lanes, supporting a data transmission of up to 1.5 Gbps per lane to communicate with camera sensors compliant with the MIPI CSI-2 specification.

Note:
The MIPI CSI-2 specification defines the communication between image application processors and cameras. It is part of the communication protocols defined by MIPI Alliance standards, designed for chip-to-chip communication in mobile systems.

40.2 Terminology

This section covers terminology used to describe the functionality of MIPI CSI.

MIPI CSI-2    MIPI Alliance Specification for Camera Serial Interface 2. It receives camera data through the PHY Protocol Interface (PPI) from the MIPI RX D-PHY and outputs data through a 32-bit image interface to the Image Signal Processor (ISP).

MIPI D-PHY   MIPI Alliance Specification for the source synchronous physical layer. It implements the physical layer of universal lanes for the MIPI D-PHY interface, which receives clock and data from MIPI camera sensors through one clock lane and two data lanes.

PPI          PHY Protocol Interface defined in MIPI Alliance Specification. It connects the CSI-2 host controller and D-PHY.

ISP          Image Signal Processor, used to process images received from the camera. For more details about ISP, please refer to Chapter 36 Image Signal Processor (ISP).

Transmitter  The device that transmits data, usually a MIPI camera.

Receiver     The device that receives data, in this chapter, the ESP32-P4 chip.

Clock lane   The clock lane of the MIPI D-PHY interface, used to transmit high-speed differential clock signals.
```