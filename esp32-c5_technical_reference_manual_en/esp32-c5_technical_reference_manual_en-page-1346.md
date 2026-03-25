

```markdown
| bmRequestType | bRequest          | wValue           | wIndex | wLength | Data         |
|---------------|-------------------|------------------|--------|---------|--------------|
| 01000000b     | 0 (VEND_JTAG_SETDIV) | [divider]        | interface | 0       | None         |
| 01000000b     | 1 (VEND_JTAG_SETIO)   | [iobits]         | interface | 0       | None         |
| 11000000b     | 2 (VEND_JTAG_GETTDO)  | 0                | interface | 1       | [iostate]    |
| 10000000b     | 6 (GET_DESCRIPTOR)    | 0x2000           | 0       | 256     | [jtag cap desc] |

- VEND_JTAG_SETDIV sets the divider used. This directly affects the duration of a TCK clock pulse. The TCK clock pulses are derived from a base clock of 48 MHz, which is divided down using an internal divider. This control request allows the host to set this divider. Note that on startup, the divider is set to 2, which means the TCK clock rate will generally be 24 MHz.
- VEND_JTAG_SETIO can bypass the JTAG command processor to set the internal TDI, TDO, TMS, and SRST lines to given values. These values are encoded in the wValue field in the format of 11'b0, srst, trst, tck, tms, tdi.
- VEND_JTAG_GETTDO can bypass the JTAG response capture unit to read the internal TDO signal directly. This request returns one byte of data, of which the least significant bit represents the status of the TDO line.
- GET_DESCRIPTOR is a standard USB request. However, it can also be used with a vendor-specific wValue of 0x2000 to get the JTAG capabilities descriptor. This returns a certain amount of bytes representing the following fixed structure, which describes the capabilities of the USB-to-JTAG adapter (as shown in Table 37.3-5). This structure allows host software to automatically support future revisions of the hardware without the need for an update.

The JTAG capability descriptors of ESP32-C5 are as follows. Note that all 16-bit values are little-endian.
```

```markdown
Table 37.3-5. JTAG Capability Descriptors

| Byte | Value | Description |
|------|-------|-------------|
| 0    | 1     | JTAG protocol capability structure version |
| 1    | 10    | Total length of JTAG protocol capabilities |
| 2    | 1     | Type of this struct: 1 for speed capability struct |
| 3    | 8     | Length of this speed capabilities struct |
| 4 ~ 5 | 4800  | JTAG base clock speed in 10 kHz increments. Note that the maximum TCK speed is half of this value |
| 6 ~ 7 | 1     | Minimum divider value settable by the VEND_JTAG_SETDIV request |
| 8 ~ 9 | 255   | Maximum divider value settable by the VEND_JTAG_SETDIV request |

## 37.4 Interrupts

ESP32-C5's USB Serial/JTAG Controller can generate the USB_SERIAL_JTAG_INTR interrupt signal that will be sent to the Interrupt Matrix. There are several internal interrupt sources from the USB Serial/JTAG Controller that can generate this interrupt signal.

- USB_SERIAL_JTAG_JTAG_IN_FLUSH_INT: triggered when flush cmd is received for the JTAG bulk out endpoint.
```