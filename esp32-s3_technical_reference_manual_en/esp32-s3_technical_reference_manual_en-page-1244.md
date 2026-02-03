**Chapter Title:**
Chapter 33 USB Serial/JTAG Controller (USB_SERIAL_JTAG)

**GoBack Link:** GoBack

**Diagram Description and Labels in Image:**
- **48 MHz clock APB clock**
- **USBD+ USBD- External USB PHY CDC-ACM Xtensa CPU cores JTAG Command Processor USB Serial/JTAG Logic**

**Figure Caption (Image):**
Figure 33.2-1. USB Serial/JTAG High Level Diagram

**Body Text:**
As shown in Figure 33.2-1, the USB Serial/JTAG Controller consists of a USB PHY, a USB device interface, a JTAG command processor and a response capture unit, as well as the CDC-ACM registers. The PHY and part of the device interface are clocked from a 48 MHz clock derived from the main PLL, the rest of the logic is clocked from APB_CLK. The JTAG command processor is connected to the JTAG debug unit of the main processor; the CDC-ACM registers are connected to the APB bus and as such can be read from and written to by software running on the main CPU.

Note that while the USB Serial/JTAG device is a USB 2.0 device, it only supports Full-speed (12 Mbps) and not the High-speed (480 Mbps) mode USB 2.0 standard introduced.

**Subsection Title:**
33.3 Functional Description

**Body Text under Subsection:**
The USB Serial/JTAG Controller interfaces with an USB host processor on one side, and the CPU debug hardware as well as the software running on the USB port on the other side.
- **33.3.1 USB Serial/JTAG Host Connection**

As shown in Figure 33.3-1, interfacing with an USB host connection on the physical level is done with a PHY. The ESP32-S3 has an internal PHY, which is shared between the USB-OTG and the USB Serial/JTAG hardware.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Version Information:** 
ESP32-S3 TRM (Version 1.7)