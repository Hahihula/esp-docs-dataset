**Title: Chapter 33 USB Serial/JTAG Controller (USB_SERIAL_JTAG)**

**Body Text:**
and optionally make it go into download mode in order to flash new firmware. This is done by setting the RTS and DTR lines on the virtual serial port.

Note that if the download mode flag is set when the ESP32-S3 is reset, the ESP32-S3 will reboot into download mode. When this flag is cleared and the chip is reset, the ESP32-S3 will boot from flash. For specific sequences, please refer to Section 33.4. All these functions can also be disabled by programming various eFuses, please refer to Chapter 5 eFuse Controller for more details.

**Subtitle: Table 33.3-2. CDC-ACM Settings with RTS and DTR**

| RTS | DTR | Action |
|-----|-----|--------|
| 0   | 0   | Clear download mode flag |
| 0   | 1   | Set download mode flag |
| 1   | 0   | Reset ESP32-S3 |
| 1   | 1   | No action |

**Subtitle: Section 33.3.3 CDC-ACM Firmware Interface Functional Description**

As the USB Serial/JTAG Controller is connected to the internal APB bus of the ESP32-S3, the CPU can interact with it. This is mainly used to read and write data from and to the virtual serial port on the attached host.

USB CDC-ACM serial data is sent to and received from the host in packets of 0 to 64 bytes in size. When enough CDC-ACM data has accumulated in the host, the host will send a packet to the CDC-ACM receive endpoint, and when the USB Serial/JTAG Controller has a free buffer, it will accept this packet. Conversely, the host will check periodically if the USB Serial/JTAG Controller has a packet ready to be sent to the host, and if so, receive this packet.

Firmware can get notified of new data from the host in one of two ways. First of all, the `USB_SERIAL_JTAG_SERIAL_OUT_EP_DATA_AVAIL` bit will remain set to 1 as long as there still is unread host data in the buffer. Secondly, the availability of data will trigger the `USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKT_INT` interrupt.

When data is available, it can be read by firmware by repeatedly reading bytes from `USB_SERIAL_JTAG_EP1_REG`. The amount of bytes to read can be determined by checking the `USB_SERIAL_JTAG_SERIAL_OUT_EP_DATA_AVAIL` bit after reading each byte to see if there is more data to read. After all data is read, the USB debug device is automatically readied to receive a new data packet from the host.

When the firmware has data to send, it can do so by putting it in the send buffer and triggering a flush, allowing the host to receive the data in a USB packet. In order to do so, there needs to be space available in the send buffer. Firmware can check this by reading `USB_REG_SERIAL_IN_EP_DATA_FREE`; a 1 in this register field indicates there is still free room in the buffer. While this is the case, firmware can fill the buffer by writing bytes to the `USB_SERIAL_JTAG_EP1_REG` register.

Writing the buffer doesn't immediately trigger sending data to the host. This does not happen until the buffer is flushed; a flush causes the entire buffer to be readied for reception by the USB host at once. A flush can be triggered in two ways: after the 64th byte is written to the buffer, the USB hardware will automatically flush the buffer to the host. Alternatively, firmware can trigger a flush by writing a `1` to `USB_REG_SERIAL_WR_DONE`.

**Footer:**  
Espressif Systems  
Page number and document version information (not fully visible): ESP32-S3 TRM (Version 1.7)