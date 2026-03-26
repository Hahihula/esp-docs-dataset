

```markdown
Register 54.10. SDHOST_CMD_REG (0x002C)

Continued from the previous page...

SDHOST_CCS_EXPECTED Configures whether to expect Command Completion Signal (CCS).
    0: Interrupts are not enabled in CE-ATA device (nIEN = 1 in ATA control register), or command does not expect CCS from CE-ATA device
    1: Interrupts are enabled in CE-ATA device (nIEN = 0), and RW_BLK command expects CCS from CE-ATA device
        (R/W)

SDHOST_VOLT_SWITCH Configures whether to enable voltage switching.
    0: No voltage switching
    1: Voltage switching enabled, must be set for CMD11 only
        (R/W)

SDHOST_USE_HOLE_REG Configures whether to use Hold Register.
    0: CMD and DATA sent to card bypassing HOLD Register
    1: CMD and DATA sent to card through the HOLD Register
        (R/W)

SDHOST_START_CMD Configures whether to to start the command.
    0: Not start
    1: Start

Once command is served by the CIU, this bit is automatically cleared.

When this bit is set, host should not attempt to write to any command registers. If a write is attempted, hardware lock error is set in raw interrupt register. (R/W/SC)
```