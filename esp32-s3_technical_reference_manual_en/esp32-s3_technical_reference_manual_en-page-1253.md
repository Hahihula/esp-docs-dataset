**Chapter Title:**
Chapter 33 USB Serial/JTAG Controller (USB_SERIAL_JTAG)

**Table Header:**
Table 33.4-2. IO Pad Status After Chip Initialization in the USB-OTG Download Mode

| VIO PAD | Input/Output Mode | Level Status |
|---------|-------------------|--------------|
| VP (MTMS) | INPUT | - |
| VM (MTDI) | INPUT | - |
| RCV (GPIO21) | INPUT | - |
| OEN (MDDO) | OUTPUT | HIGH |
| VPO (MTCK) | OUTPUT | LOW |
| VMQ (GPIO38) | OUTPUT | LOW |

**Section Title:**
33.4.2 Runtime Operation

**Body Text:**

There is very little setup needed in order to use the USB Serial/JTAG Device. The USB-to-JTAG hardware itself does not need any setup aside from the standard USB initialization the host operating system already does.

The CDC-ACM emulation, on the host side, also is plug-and-play.

On the firmware side, very little initialization should be needed either: the USB hardware is self-initializing and after boot-up, if a host is connected and listening on the CDC-ACM interface, data can be exchanged as described above without any specific setup aside from the firmware optionally setting up an interrupt service handler.

One thing to note is that there may be situations where the host is either not attached or the CDC-ACM virtual port is not opened. In this case, the packets that are flushed to the host will never be picked up and the transmit buffer will never be empty. It is important to detect this and time out as this is the only way to reliably detect that the port on the host side is closed.

Another thing to note is that the USB device is dependent on both the PLL for the 48 MHz USB PHY clock, as well as APB_CLK. Specifically, an APB_CLK of 40 MHz or more is required for proper USB compliant operation; although the USB device will still function with most hosts with an APB_CLK as low as 10 MHz. Behaviour shown when this happens is dependent on the host USB hardware and drivers, and can include the device being unresponsive and it disappearing when first accessed.

More specifically, the APB_CLK will be affected by clock gating the USB Serial/JTAG Controller, which may happen in Light-sleep. Additionally, the USB serial/JTAG Controller (as well as the attached Xtensa CPUs) will be entirely powered down in Deep-sleep mode. If a device needs to be debugged in either of these two modes, it may be preferable to use an external JTAG debugger and serial interface instead.

The CDC-ACM interface can also be used to reset the SoC and take it into or out of download mode. Generating the correct sequence of handshake signals can be a bit complicated: Most operating systems only allow setting or resetting DTR and RTS separately, not in tandem. Additionally, some drivers (e.g., the standard CDC-ACM driver on Windows) do not set DTR until RTS is set and the user needs to explicitly set RTS in order to 'propagate' the DTR value. These are the recommended procedures:

To reset the SoC into download mode: 

**Footer Information:** 
Espressif Systems  
ESP32-S3 TRM (Version 1.7)