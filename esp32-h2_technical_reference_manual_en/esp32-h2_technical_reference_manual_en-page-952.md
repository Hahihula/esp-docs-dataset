

```markdown
Figure 33.2-2. USB Serial/JTAG Block Diagram

33.3 Functional Description

The USB Serial/JTAG controller interfaces with a USB host processor on one side, and with the CPU debugging hardware as well as the software that communicates through the CDC-ACM port on the other side.

33.3.1 CDC-ACM USB Interface Functional Description

The CDC-ACM interface adheres to the standard USB CDC-ACM class for serial port emulation. It contains a dummy interrupt endpoint (which will never send any events, as they are not implemented nor needed) and a Bulk IN as well as a Bulk OUT endpoint for the host's received and sent serial data respectively. These endpoints can handle 64-byte packets at a time, allowing high throughput. As CDC-ACM is a standard USB device class, a host generally can function without any special installation procedures. That is to say, when the USB debugging device is properly connected to a host, the operating system should show a new serial port moments later.

The CDC-ACM interface accepts the following standard CDC-ACM control requests:

Table 33.3-1. Standard CDC-ACM Control Requests

| Command                  | Action                                                                 |
|--------------------------|------------------------------------------------------------------------|
| SEND_BREAK               | Accepted but ignored (dummy)                                          |
| SET_LINE_CODING          | Accepted, value sent is readable in software                          |
| GET_LINE_CODING          | By default, returns 9600 baud, no parity, 8 databits, 1 stopbit (Can be changed through software) |
| SET_CONTROL_LINE_STATE   | Set the state of the RTS/DTR lines. See Table 33.3-2                  |

Aside from general-purpose communication, the CDC-ACM interface can also be used to reset ESP32-H2 and optionally make it enter download mode to flash new firmware. This can be realized by setting the RTS and
```