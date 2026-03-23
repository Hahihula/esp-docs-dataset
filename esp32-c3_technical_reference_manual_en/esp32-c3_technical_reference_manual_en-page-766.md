

```markdown
Figure 30.2-2. USB Serial/JTAG Block Diagram

Table 30.3-1. Standard CDC-ACM Control Requests

| Command                  | Action                                                                 |
|--------------------------|-------------------------------------------------------------------------|
| SEND_BREAK               | Accepted but ignored (dummy)                                           |
| SET_LINE_CODING          | Accepted but ignored (dummy)                                           |
| GET_LINE_CODING          | Always returns 9600 baud, no parity, 8 databits, 1 stopbit             |
| SET_CONTROL_LINE_STATE   | Set the state of the RTS/DTR lines, see Table 30.3-2                   |

Aside from general-purpose communication, the CDC-ACM interface also can be used to reset the ESP32-C3 and optionally make it go into download mode in order to flash new firmware. This is done by setting the RTS and DTR lines on the virtual serial port.

Table 30.3-2. CDC-ACM Settings with RTS and DTR

| RTS | DTR | Action                        |
|-----|-----|--------------------------------|
| 0   | 0   | Clear download mode flag      |
| 0   | 1   | Set download mode flag        |
| 1   | 0   | Reset ESP32-C3                 |
| 1   | 1   | No action                     |

Note that if the download mode flag is set when the ESP32-C3 is reset, the ESP32-C3 will reboot into download mode. When this flag is cleared and the chip is reset, the ESP32-C3 will boot from flash. For specific sequences, please refer to Section 30.4. All these functions can also be disabled by programming various eFuses, please refer to Chapter 4 eFuse Controller (EFUSE) for more details.
```