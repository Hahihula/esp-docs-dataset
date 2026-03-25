

```markdown
| RTS | DTR | Action                     |
|-----|-----|----------------------------|
| 0   | 0   | Clear download mode flag   |
| 0   | 1   | Set download mode flag     |
| 1   | 0   | Reset ESP32-C61            |
| 1   | 1   | No action                  |

Note that if the download mode flag is set when ESP32-C61 is reset, ESP32-C61 will reboot into download mode. When this flag is cleared and the chip is reset, ESP32-C61 will boot from flash. For specific sequences, please refer to Section 29.5. All these functions can also be disabled by programming various eFuses. Please refer to Chapter 5 eFuse Controller (EFUSE) for more details.
```

## 29.3.2 CDC-ACM Firmware Interface Functional Description

The CPU can interact with the USB Serial/JTAG controller as the module is connected to the internal APB bus of ESP32-C61. This is mainly used to read and write data from and to the virtual serial port on the attached host.

USB CDC-ACM serial data is sent to and received from the host in packets of 0 to 64 bytes in size. When enough CDC-ACM data has accumulated in the host, the host sends a packet to the CDC-ACM receive endpoint, and the USB Serial/JTAG controller accepts this packet if it has a free buffer. Conversely, the host checks periodically if the USB Serial/JTAG controller has a packet ready to be sent to the host, and if so, receives this packet.

Firmware can get notified of new data from the host in one of the following two ways. First of all, the `USB_SERIAL_JTAG_SERIAL_OUT_EP_DATA_AVAIL` bit will remain set as long as there still is unread host data in the buffer. Secondly, the availability of data will trigger the `USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKT_INT` interrupt. When data is available, it can be read by firmware through repeatedly reading bytes from `USB_SERIAL_JTAG_EP1_REG`. The amount of bytes to read can be determined by checking the `USB_SERIAL_JTAG_SERIAL_OUT_EP_DATA_AVAIL` bit after reading each byte to see if there is more data to read. After all data is read, the USB device is automatically readied to receive a new data packet from the host.

Generally, after sending data, the attached host will block until the data is actually read by firmware in one of the described methods. However, it is possible that a given firmware program does not read data at all. This situation generally is not expected by host programs which are written to talk to a discrete USB-serial converter; the program e.g. stops executing until the data is read. The ESP32-C61 USB-serial-JTAG adapter can simulate the behavior of a discrete USB-serial-JTAG converter: by writing a timeout to `USB_SERIAL_JTAG_SERIAL_TIMEOUT_MAX` and writing an 1 to `USB_SERIAL_JTAG_SERIAL_TIMEOUT_EN`, any unread data will be automatically flushed after the given timeout.

When the firmware has data to send, it can put the data in the send buffer and trigger a flush to allow the host to receive the data in a USB packet. In order to do so, there needs to be space available in the send buffer. Firmware can check this by reading `USB_REG_SERIAL_IN_EP_DATA_FREE`. A 1 in this register field indicates
```