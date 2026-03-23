
```markdown
| bmRequestType | bRequest          | wValue           | wIndex | wLength | Data         |
|---------------|-------------------|------------------|--------|---------|--------------|
| 01000000b     | 0 (VEND_JTAG_SETDIV) | [divider]        | interface | 0       | None         |
| 01000000b     | 1 (VEND_JTAG_SETIO)   | [iobits]         | interface | 0       | None         |
| 11000000b     | 2 (VEND_JTAG_GETTDO)  | 0                | interface | 1       | [iostate]    |
| 10000000b     | 6 (GET_DESCRIPTOR)   | 0x2000           | 0       | 256     | [jtag cap desc] |

- VEND_JTAG_SETDIV sets the divider used. This directly affects the duration of a TCK clock pulse. The TCK clock pulses are derived from APB_CLK, which is divided down using an internal divider. This control request allows the host to set this divider. Note that on startup, the divider is set to 2, meaning the TCK clock rate will generally be 40 MHz.
- VEND_JTAG_SETIO can bypass the JTAG command processor to set the internal TDI, TDO, TMS and SRST lines to given values. These values are encoded in the wValue field in the format of 11'bO, srst, trst, tck, tms, tdi.
- VEND_JTAG_GETTDO can bypass the JTAG response capture unit to read the internal TDO signal directly. This request returns one byte of data, of which the least significant bit represents the status of the TDO line.
- GET_DESCRIPTOR is a standard USB request, however it can also be used with a vendor-specific wValue of 0x2000 to get the JTAG capabilities descriptor. This returns a certain amount of bytes representing the following fixed structure, which describes the capabilities of the USB-to-JTAG adapter. This structure allows host software to automatically support future revisions of the hardware without needing an update.

The JTAG capabilities descriptor of the ESP32-C3 is as follows. Note that all 16-bit values are little-endian.
```

```markdown
Table 30.3-5. JTAG Capabilities Descriptor

| Byte | Value | Description                                                                 |
|------|-------|-----------------------------------------------------------------------------|
| 0    | 1     | JTAG protocol capabilities structure version                                |
| 1    | 10    | Total length of JTAG protocol capabilities                                  |
| 2    | 1     | Type of this struct: 1 for speed capabilities struct                        |
| 3    | 8     | Length of this speed capabilities struct                                    |
| 4 ~ 5| 8000  | APB_CLK speed in 10 kHz increments. Note that the maximal TCK speed is half of this |
| 6 ~ 7| 1     | Minimum divisor settable by the VEND_JTAG_SETDIV request                    |
| 8 ~ 9| 255   | Maximum divisor settable by the VEND_JTAG_SETDIV request                    |

## 30.4 Recommended Operation
```