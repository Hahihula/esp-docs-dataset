

```markdown
| RTS | DTR | Action                     |
|-----|-----|----------------------------|
| 0   | 0   | Clear download mode flag   |
| 0   | 1   | Set download mode flag     |
| 1   | 0   | Reset ESP32-H2             |
| 1   | 1   | No action                  |

Note that if the download mode flag is set when ESP32-H2 is reset, ESP32-H2 will reboot into download mode. When this flag is cleared and the chip is reset, ESP32-H2 will boot from flash. For specific sequences, please refer to Section 33.4. All these functions can also be disabled by programming various eFuses. Please refer to Chapter 5 eFuse Controller (EFUSE) for more details.

## 33.3.2 CDC-ACM Firmware Interface Functional Description

The CPU can interact with the USB Serial/JTAG controller as the module is connected to the internal APB bus of ESP32-H2. This is mainly used to read and write data from and to the virtual serial port on the attached host.

USB CDC-ACM serial data is sent to and received from the host in packets of 0 to 64 bytes in size. When enough CDC-ACM data has accumulated in the host, the host sends a packet to the CDC-ACM receive endpoint, and the USB Serial/JTAG controller accepts this packet if it has a free buffer. Conversely, the host checks periodically if the USB Serial/JTAG controller has a packet ready to be sent to the host, and if so, receives this packet.

Firmware can get notified of new data from the host in one of the following two ways. First of all, the `USB_SERIAL_JTAG_SERIAL_OUT_EP_DATA_AVAIL` bit will remain set as long as there still is unread host data in the buffer. Secondly, the availability of data will trigger the `USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKT_INT` interrupt. When data is available, it can be read by firmware through repeatedly reading bytes from `USB_SERIAL_JTAG_EP1_REG`. The amount of bytes to read can be determined by checking the `USB_SERIAL_JTAG_SERIAL_OUT_EP_DATA_AVAIL` bit after reading each byte to see if there is more data to read. After all data is read, the USB debugging device is automatically reaided to receive a new data packet from the host.

When the firmware has data to send, it can put the data in the send buffer and trigger a flush to allow the host to receive the data in a USB packet. In order to do so, there needs to be space available in the send buffer. Firmware can check this by reading `USB_REG_SERIAL_IN_EP_DATA_FREE`. A 1 in this register field indicates there is still free room in the buffer, and firmware can fill the buffer by writing bytes to the `USB_SERIAL_JTAG_EP1_REG` register. Writing to the buffer does not immediately trigger sending data to the host until the buffer is flushed. After the flush, the entire buffer will be ready to be received by the USB host at once. A flush can be triggered in two ways: 1) after the 64th byte is written to the buffer, the USB hardware will automatically flush the buffer to the host; or 2) firmware can trigger a flush by writing 1 to `USB_SERIAL_JTAG_WR_DONE`.

Regardless of how a flush is triggered, the send buffer will be unavailable for firmware to write into until it has been fully read by the host. As soon as the send buffer has been fully read, the `USB_SERIAL_JTAG_`
```