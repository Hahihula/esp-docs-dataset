

```markdown
Register 54.1. CTRL_REG (0x0000)

Continued from the previous page...

SDHOST_SEND_IRQ_RESPONSE Configures whether to send auto interrupt request (IRQ) response.
This bit automatically clears once a response is sent.
To wait for MMC card interrupts, the host issues a CMD40 command and waits for an interrupt
response from MMC card(s). In the meantime, if the host wants SD/MMC to exit waiting for
the interrupt state, it can set this bit, at which time SD/MMC command state-machine sends a
CMD40 response on the bus and returns to the idle state.
0: No effect
1: Send auto IRQ response
(R/W)

SDHOST_ABORT_READ_DATA Configures whether to abort read data. This bit is automatically
cleared once the data state machine is reset to idle.
After a suspend-command is issued during a read-operation, software polls the card to find
when the suspend-event occurred. Once the suspend-event has occurred, software sets the
bit which will reset the data state machine that is waiting for the next block of data.
0: No effect
1: Abort read data
(R/W)

SDHOST_SEND_CCSD Configures whether to send Command Completion Signal Disable (CCSD) to
CE-ATA device. Once the CCSD pattern is sent to the device, SD/MMC automatically clears the
SDHOST_SEND_CCSD bit. It also sets the Command Done (CD) bit in the SDHOST_RINTSTS_REG
register.
Software sets this bit only if the current command is expecting CCS (that is, RW_BLK), and if
interrupts are enabled for the CE-ATA device.
0:No effect
1: Send CCSD to CE-ATA device
(R/W)

SDHOST_SEND_AUTO_STOP_CCSD Configures whether to send an internally-generated STOP
command (CMD12) to the CE-ATA device. After sending the CCSD, SD/MMC automatically clears
the SDHOST_SEND_AUTO_STOP_CCSD bit. After sending this internally-generated STOP command,
the Auto Command Done (ACD) bit in SDHOST_RINTSTS_REG is set.
Always Set SDHOST_SEND_AUTO_STOP_CCSD and SDHOST_SEND_CCSD bits together, SD-
HOST_SEND_AUTO_STOP_CCSD should not be set independently of SDHOST_SEND_CCSD.
0:No effect
1: Send internally-generated STOP command (CMD12) to the CE-ATA device
(R/W)

Continued on the next page...
```