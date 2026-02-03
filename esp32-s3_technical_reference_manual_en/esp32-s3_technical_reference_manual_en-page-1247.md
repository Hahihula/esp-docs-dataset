**Chapter Title:**
Chapter 33 USB Serial/JTAG Controller (USB_SERIAL_JTAG)

**Body Text:**
The CPU JTAG signals can be routed to the USB Serial/JTAG Controller or external GPIO pads using eFuses and when the user program has started, software control as well. At that time, the JTAG signals from the USB Serial/JTAG can also be routed to the GPIO matrix. This allows debugging a secondary SoC via JTAG using the ESP32-S3 USB Serial/JTAG Controller.

**Diagram Description:**
- **Figure 33.3-2. JTAG Routing Diagram:** 
  - The diagram shows connections from "USB JTAG" and "GPIO matrix Pad JTAG".
  - Arrows indicate routing paths to different points labeled as `3'b100`, `3'bx10`, `3'bx01`, `3'bx11`.
  - There is a connection between the CPU, USB JTAG, and GPIO matrix.
  - Labels include "USB JTAG_BRIDGE_EN", "usb_jtag: JTAG signals come from USB Serial/JTAG Controller" with control selection `ctrl_sel[2:0]`, and other labels like `pad_jtag: JTAG signals come from MTMS/MTCK/MTDI/MTDO pads` indicating connections to `ctrl_sel[1]`, `ctrl_sel[0]`.

**Subsection Title:**
33.3.2 CDC-ACM USB Interface Functional Description

**Body Text under Subsection:**
The CDC-ACM interface adheres to the standard USB CDC-ACM class for serial port emulation. It contains a dummy interrupt endpoint (which will never send any events, as they are not implemented nor needed) and a Bulk IN as well as a Bulk OUT endpoint for the host’s received and sent serial data respectively. These endpoints can handle 64-byte packets at a time, allowing for high throughput. As CDC-ACM is a standard USB device class, a host generally does not need any special installation procedures for it to function: when the USB debugging device is properly connected to a host, the operating system should show a new serial port moments later.

The CDC-ACM interface accepts the following standard CDC-ACM control requests:

**Table Title and Content:**
Table 33.3-1. Standard CDC-ACM Control Requests

| Command                   | Action                           |
|---------------------------|----------------------------------|
| SEND_BREAK               | Accepted but ignored (dummy)     |
| SET_LINE_CODING           | Accepted but ignored (dummy)     |
| GET_LINE_CODING           | Always returns 9600 baud, no parity, 8 databits, 1 stopbit |
| SET_CONTROL_LINE_STATE   | Set the state of the RTS/DTR lines, see Table 33.3-2 |

**Additional Information:**
Aside from general-purpose communication, the CDC-ACM interface also can be used to reset the ESP32-S3 Espressif Systems.

**Footer Text and Link:**
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback

**Page Number:** 
1247