

```markdown
## 30.3.2 CDC-ACM Firmware Interface Functional Description

As the USB Serial/JTAG Controller is connected to the internal APB bus of the ESP32-C3, the CPU can interact with it. This is mainly used to read and write data from and to the virtual serial port on the attached host.

USB CDC-ACM serial data is sent to and received from the host in packets of 0 to 64 bytes in size. When enough CDC-ACM data has accumulated in the host, the host will send a packet to the CDC-ACM receive endpoint, and when the USB Serial/JTAG Controller has a free buffer, it will accept this packet. Conversely, the host will check periodically if the USB Serial/JTAG Controller has a packet ready to be sent to the host, and if so, receive this packet.

Firmware can get notified of new data from the host in one of two ways. First of all, the `USB_SERIAL_JTAG_SERIAL_OUT_EP_DATA_AVAIL` bit will remain set to one as long as there still is unread host data in the buffer. Secondly, the availability of data will trigger the `USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKT_INT` interrupt as well.

When data is available, it can be read by firmware by repeatedly reading bytes from `USB_SERIAL_JTAG_EP1_REG`. The amount of bytes to read can be determined by checking the `USB_SERIAL_JTAG_SERIAL_OUT_EP_DATA_AVAIL` bit after reading each byte to see if there is more data to read. After all data is read, the USB debug device is automatically readied to receive a new data packet from the host.

When the firmware has data to send, it can do so by putting it in the send buffer and triggering a flush, allowing the host to receive the data in a USB packet. In order to do so, there needs to be space available in the send buffer. Firmware can check this by reading `USB_REG_SERIAL_IN_EP_DATA_FREE`; a one in this register field indicates there is still free room in the buffer. While this is the case, firmware can fill the buffer by writing bytes to the `USB_SERIAL_JTAG_EP1_REG` register.

Writing the buffer doesn't immediately trigger sending data to the host. This does not happen until the buffer is flushed; a flush causes the entire buffer to be readied for reception by the USB host at once. A flush can be triggered in two ways: after the 64th byte is written to the buffer, the USB hardware will automatically flush the buffer to the host. Alternatively, firmware can trigger a flush by writing a one to `USB_REG_SERIAL_WR_DONE`.

Regardless of how a flush is triggered, the send buffer will be unavailable for firmware to write into until it has been fully read by the host. As soon as this happens, the `USB_SERIAL_JTAG_SERIAL_IN_EMPTY_INT` interrupt will be triggered, indicating the send buffer can receive another 64 bytes.

## 30.3.3 USB-to-JTAG Interface

The USB-to-JTAG interface uses a vendor-specific class for its implementation. It consists of two endpoints, one to receive commands and one to send responses. Additionally, some less time-sensitive commands can be given as control requests.

## 30.3.4 JTAG Command Processor

Commands from the host to the JTAG interface are interpreted by the JTAG command processor. Internally, the JTAG command processor implements a full four-wire JTAG bus, consisting of the TCK, TMS and TDI output lines to the RISC-V CPU, as well as the TDO line signalling back from the CPU to the JTAG response
```