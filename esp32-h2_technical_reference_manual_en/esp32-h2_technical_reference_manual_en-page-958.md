

```markdown
One scenario where this happens is Deep-sleep. The USB Serial/JTAG controller (as well as the attached RISC-V CPU) will be entirely powered down in Deep-sleep mode. If a device needs to be debugged in this mode, it may be preferable to use an external JTAG debugger and a serial interface instead.

The CDC-ACM interface can also be used to reset the SoC and take it into or out of download mode. Generating the correct sequence of handshake signals can be a bit complicated, since most operating systems only allow setting or clearing DTR and RTS separately, but not in tandem. Additionally, some drivers (e.g., the standard CDC-ACM driver on Windows) do not set DTR until RTS is set and the user needs to explicitly set RTS in order to ‘propagate’ the DTR value. The recommended procedures are introduced below.

To reset the SoC into download mode:

**Table 33.4-1. Reset SoC into Download Mode**

| Action           | Internal state   | Note                          |
|------------------|------------------|--------------------------------|
| Clear DTR        | RTS=?, DTR=0     | Initialize to known values     |
| Clear RTS        | RTS=0, DTR=0     | -                              |
| Set DTR          | RTS=0, DTR=1     | Set download mode flag         |
| Clear RTS        | RTS=0, DTR=1     | Propagate DTR                  |
| Set RTS          | RTS=1, DTR=1     | -                              |
| Clear DTR        | RTS=1, DTR=0     | Reset SoC                      |
| Set RTS          | RTS=1, DTR=0     | Propagate DTR                  |
| Clear RTS        | RTS=0, DTR=0     | Clear download flag            |

To reset the SoC into booting from flash:

**Table 33.4-2. Reset SoC into Booting from flash**

| Action           | Internal state   | Note                          |
|------------------|------------------|--------------------------------|
| Clear DTR        | RTS=?, DTR=0     | -                              |
| Clear RTS        | RTS=0, DTR=0     | Clear download flag            |
| Set RTS          | RTS=1, DTR=0     | Reset SoC                      |
| Clear RTS        | RTS=0, DTR=0     | Exit reset                     |

### 33.5 Interrupts

*   USB_SERIAL_JTAG_JTAG_IN_FLUSH_INT: triggered when flush cmd is received for IN endpoint 2 of JTAG.
*   USB_SERIAL_JTAG_SOF_INT: triggered when SOF frame is received.
*   USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKT_INT: triggered when Serial Port OUT Endpoint receives one packet.
*   USB_SERIAL_JTAG_SERIAL_IN_EMPTY_INT: triggered when Serial Port IN Endpoint is empty.
*   USB_SERIAL_JTAG_PID_ERR_INT: triggered when PID error is detected.
*   USB_SERIAL_JTAG_CRC5_ERR_INT: triggered when CRC5 error is detected.
```