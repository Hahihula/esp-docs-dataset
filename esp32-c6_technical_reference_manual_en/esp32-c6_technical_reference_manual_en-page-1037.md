

```markdown
| Action                  | Internal state   | Note                     |
|-------------------------|------------------|--------------------------|
| Clear DTR               | RTS=?, DTR=0     | Initialize to known values |
| Clear RTS               | RTS=0, DTR=0     | -                        |
| Set DTR                 | RTS=0, DTR=1     | Set download mode flag   |
| Clear RTS               | RTS=0, DTR=1     | Propagate DTR            |
| Set RTS                 | RTS=1, DTR=1     | -                        |
| Clear DTR               | RTS=1, DTR=0     | Reset SoC                |
| Set RTS                 | RTS=1, DTR=0     | Propagate DTR            |
| Clear RTS               | RTS=0, DTR=0     | Clear download flag      |

To reset the SoC into booting from flash:

Table 32.4-2. Reset SoC into Booting from flash

| Action                  | Internal state   | Note                     |
|-------------------------|------------------|--------------------------|
| Clear DTR               | RTS=?, DTR=0     | -                        |
| Clear RTS               | RTS=0, DTR=0     | Clear download flag      |
| Set RTS                 | RTS=1, DTR=0     | Reset SoC                |
| Clear RTS               | RTS=0, DTR=0     | Exit reset               |

## 32.5 Interrupts

*   USB_SERIAL_JTAG_JTAG_IN_FLUSH_INT: triggered when flush cmd is received for IN endpoint 2 of JTAG.
*   USB_SERIAL_JTAG_SOF_INT: triggered when SOF frame is received.
*   USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKT_INT: triggered when Serial Port OUT Endpoint receives one packet.
*   USB_SERIAL_JTAG_SERIAL_IN_EMPTY_INT: triggered when Serial Port IN Endpoint is empty.
*   USB_SERIAL_JTAG_PID_ERR_INT: triggered when PID error is detected.
*   USB_SERIAL_JTAG_CRC5_ERR_INT: triggered when CRC5 error is detected.
```