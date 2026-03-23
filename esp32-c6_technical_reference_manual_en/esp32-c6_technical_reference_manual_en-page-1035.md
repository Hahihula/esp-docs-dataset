

```markdown
3. TCK is clocked with the TDI line set to 0 and TMS set to 1. Data on the TDO line is captured.
4. TCK is clocked another (1 × 2 + 0) × (4⁰) = 2 times with the same settings as step 3.
5. Nothing happens: (0 × 2 + 0) × (4¹) = 0. Note that this increases cmd_rep_count in the next step.
6. TCK is clocked another (1 × 2 + 1) × (4²) = 48 times with the same settings as step 3.

In other words, this example stream has the same net effect as that of executing command 1 twice, then repeating command 3 for 51 times.
```

### 32.3.5 USB-to-JTAG Interface: Response Capture Unit

The response capture unit reads the TDO line of the internal JTAG bus and captures its value when the command parser executes a CMD_CLK with cap=1. It puts this bit into an internal shift register, and writes a byte into the USB buffer when 8 bits have been collected. Of these 8 bits, the least significant one is the one that is read from TDO the earliest.

As soon as either 64 bytes (512 bits) have been collected or a CMD_FLUSH command is executed, the response capture unit will make the buffer available for the host to receive. Note that the interface to the USB logic is double-buffered. Therefore, as long as the USB throughput is sufficient, the response capture unit can always receive more data. That is to say, while one of the buffers is waiting to be sent to the host, the other can receive more data. When the host has received data from its buffer and the response capture unit flushes its buffer, the two buffers exchange position.

This also means that a command stream can cause at most 128 bytes of capture data generated (less if there are flush commands in the stream) without the host acting to receive the generated data. If more data is generated anyway, the command stream will pause and the device will not accept more commands until the generated capture data is read out.

Note that in general, the logic of the response capture unit tries not to send zero-byte responses. For instance, sending a series of CMD_FLUSH commands will not cause a series of 0-byte USB responses to be sent. However, in the current implementation, some zero-0 responses may be generated in extraordinary circumstances. It is recommended to ignore these responses.

### 32.3.6 USB-to-JTAG Interface: Control Transfer Requests

Aside from the command processor and the response capture unit, the USB-to-JTAG interface also understands some control requests, as documented in the table below:

**Table 32.3-4. USB-to-JTAG Control Requests**

| bmRequestType | bRequest | wValue     | wIndex | wLength | Data         |
|---------------|----------|------------|--------|---------|--------------|
| 01000000b      | 0 (VEND_JTAG_SETDIV) | [divider]   | interface | 0       | None         |
| 01000000b      | 1 (VEND_JTAG_SETIO)  | [iobits]    | interface | 0       | None         |
| 11000000b      | 2 (VEND_JTAG_GETTDO) | 0          | interface | 1       | [iostate]    |
| 10000000b      | 6 (GET_DESCRIPTOR)   | 0x2000     | 0      | 256     | [jtag cap desc] |

* VEND_JTAG_SETDIV sets the divider used. This directly affects the duration of a TCK clock pulse. The TCK clock pulses are derived from a base clock of 48 MHz, which is divided down using an internal
```