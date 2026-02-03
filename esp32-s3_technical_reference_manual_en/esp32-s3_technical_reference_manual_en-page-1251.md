**Chapter Title:**
Chapter 33 USB Serial/JTAG Controller (USB_SERIAL_JTAG)

**Body Text:**
more data. When the host has received data from its buffer and the response capture unit flushes its buffer, the two buffers change position.

This also means that a command stream can cause at most 128 bytes of capture data to be generated (less if there are flush commands in the stream) without the host acting to receive the generated data. If more data is generated anyway, the command stream is paused and the device will not accept more commands before the generated capture data is read out.

Note that in general, the logic of the response capture unit tries not to send zero-byte responses: for instance, sending a series of CMD_FLUSH commands will not cause a series of zero-byte USB responses to be sent. However, in the current implementation, some zero-byte responses may be generated in extraordinary circumstances. It’s recommended to ignore these responses.

**Subheading and Subsection Title:**
33.3.8 USB-to-JTAG Interface: Control Transfer Requests

**Body Text under Subsection:**
Aside from the command processor and the response capture unit, the USB-to-JTAG interface also understands some control requests, as documented in the table below:

**Table Title:**
Table 33.3-4. USB-to-JTAG Control Requests

| bmRequestType | bRequest       | wValue     | wIndex | DataLength | Data |
|----------------|-----------------|------------|--------|------------|------|
| 01000000b      | VEND_JTAG_SETDIV | [divider]   | interface | O         | None |
| 01000000b      | VEND_JTAG_SETIO  | [iobits]    | interface | O         | None |
| 11000000b      | VEND_JTAG_GETTDO |          | interface | I        | [jtag cap desc] |
| 10000000b      | GET_DESCRIPTOR   | 0x2000     |         | O         | 256 |

**Body Text under Table:**
- VEND_JTAG_SETDIV sets the divider used. This directly affects the duration of a TCK clock pulse. The TCK clock pulses are derived from APB_CLK, which is divided down using an internal divider. This control request allows the host to set this divider. Note that on startup, the divider is set to 2, meaning the TCK clock rate will generally be 40 MHz.
- VEND_JTAG_SETIO can bypass the JTAG command processor to set the internal TDI, TDO, TMS and SRST lines to given values. These values are encoded in the wValue field in the format of 11'b0, srst, trst, tck, tms, tdi.
- VEND_JTAG_GETTDO can bypass the JTAG response capture unit to read the internal TDO signal directly. This request returns one byte of data, of which the least significant bit represents the status of the TDO line.

**Additional Information:**
GET_DESCRIPTOR is a standard USB request; however it can also be used with a vendor-specific wValue of 0x2000 to get the JTAG capabilities descriptor. This returns a certain amount of bytes representing the following fixed structure, which describes the capabilities of the USB-to-JTAG adapter. This structure allows host software to automatically support future revisions of the hardware without needing an update.

The JTAG capabilities descriptor of the ESP32-S3 is as follows. Note that all 16-bit values are little-endian.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Version Information:**
ESP32-S3 TRM (Version 1.7)