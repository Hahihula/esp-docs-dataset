

```markdown
Chapter 27 UART Controller (UART, LP_UART, UHCI)                                     GoBack


Register 27.71. UHCI_CONF1_REG (0x0014)


Continued from the previous page...


UHCI_WAIT_SW_START   Configures whether or not to put the UHCI encoder state machine to ST_SW_WAIT state.
                      O: No
                      1: Yes
                      (R/W)

UHCI_SW_START    Configures whether or not to send data packets when the encoder state machine is in ST_SW_WAIT state.
                 O: Not send
                 1: Send
                 (R/W/SC)
```