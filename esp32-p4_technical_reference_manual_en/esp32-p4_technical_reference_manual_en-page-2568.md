

```markdown
Chapter 51 USB Serial/JTAG Controller (USB_SERIAL_JTAG)
GoBack

been fully read by the host. As soon as the send buffer has been fully read, the
USB_SERIAL_JTAG_SERIAL_IN_EMPTY_INT interrupt will be triggered, indicating that the send buffer can
receive another 64 bytes.

It is possible to handle some out-of-band serial requests in software, specifically, the host setting DTR and RTS
and changing the line state. If the CDC-ACM interface receives a SET_LINE_CODING request, the peripheral
can be configured to trigger a USB_SERIAL_JTAG_SET_LINE_CODE_INT interrupt, at which point the line
coding can be read from the USB_SERIAL_JTAG_SET_LINE_CODE_WO_REG register. Similarly,
SET_CONTROL_LINE_STATE requests will trigger USB_SERIAL_JTAG_RTS_CHG_INT and
USB_SERIAL_JTAG_DTR_CHG_INT interrupts if they change the state of these lines. Software can then read
the specific state through the USB_SERIAL_JTAG_RTS and USB_SERIAL_JTAG_DTR bits. Note that as
described earlier, certain RTS/DTR sequences lead to hardware reset of ESP32-P4. Software can disable
hardware recognition of these DTR/RTS sequences by setting the
USB_SERIAL_JTAG_USB_UART_CHIP_RST_DIS bit, allowing software to interpret these signals freely.

Finally, the host can read the current line state using GET_LINE_CODING. This event sends back the data in the
USB_SERIAL_JTAG_GET_LINE_CODE_WO_REG register and triggers a
USB_SERIAL_JTAG_GET_LINE_CODE_INT interrupt.

51.3.3 USB-to-JTAG Interface: JTAG Command Processor

The USB-to-JTAG interface uses a vendor-specific class for its implementation. It consists of two endpoints,
one to receive commands and another to send responses. Additionally, some less time-sensitive commands
can be given as control requests.

Commands from the host to the JTAG interface are interpreted by the JTAG command processor. Internally,
the JTAG command processor implements a full four-wire JTAG bus, consisting of the TCK, TMS and TDI
output lines to the RISC-V CPU, as well as the TDO line signalling back from the CPU to the JTAG response
capture unit. These signals adhere to the IEEE 1149.1 JTAG standards. Additionally, there is an SRST line to
reset ESP32-P4.

Optionally, software can set USB_SERIAL_JTAG_USB_JTAG_BRIDGE_EN in order to redirect these signals to
the GPIO matrix instead, where they can be routed to IO pads on ESP32-P4. This also allows external devices
to be debugged via the USB Serial/JTAG peripheral.

The JTAG command processor parses each received nibble (4-bit value) as a command. As USB data is
received in 8-bit bytes, this means each byte contains two commands. The USB command processor will
execute high-nibble first and low-nibble second. The commands are used to control the TCK, TMS, TDI, and
SRST lines of the internal JTAG bus, as well as to signal the JTAG response capture unit the state of the TDO
line (which is driven by the CPU debugging logic) that needs to be captured.

In the internal JTAG bus, TCK, TMS, TDI, and TDO are connected directly to the JTAG debugging logic of the
RISC-V CPU. SRST is connected to the reset logic of the digital circuitry in ESP32-P4 and a high level on this
line will cause a digital system reset. Note that the USB Serial/JTAG controller itself is not affected by
SRST.

A nibble can contain the following commands:
```