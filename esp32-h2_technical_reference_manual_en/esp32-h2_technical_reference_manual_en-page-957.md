

```markdown
| Byte | Value | Description |
| :---- | :----- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 0 | 1 | JTAG protocol capability structure version |
| 1 | 10 | Total length of JTAG protocol capabilities |
| 2 | 1 | Type of this struct: 1 for speed capability struct |
| 3 | 8 | Length of this speed capabilities struct |
| 4 ~ 5 | 4800 | JTAG base clock speed in 10 kHz increments. Note that the maximum TCK speed is half of this value |
| 6 ~ 7 | 1 | Minimum divider value settable by the VEND_JTAG_SETDIV request |
| 8 ~ 9 | 255 | Maximum divider value settable by the VEND_JTAG_SETDIV request |
```

## 33.4 Recommended Operation

Little setup is needed for using the USB Serial/JTAG device. The USB-to-JTAG hardware itself does not need any setup aside from the standard USB initialization that the host operating system already does. Apart from that, the CDC-ACM emulation on the host side is also plug-and-play.

On the firmware side, very little initialization is needed either. The USB hardware is self-initialized and after boot-up, if a host is connected and listening on the CDC-ACM interface, data can be exchanged as described above without any specific setup except for the situation when the firmware optionally sets up an interrupt service handler.

One thing to note is that there may be situations where either the host is not attached or the CDC-ACM virtual port is not opened. In such cases, the packets that are flushed to the host will never be picked up and the send buffer will never be empty. It is important to detect these situations and implement timeout, as this is the only way to reliably detect whether the port on the host side is closed or not.

Another thing to note is that the USB device is dependent on the BBPLL for the 48 MHz USB PHY clock. If this PLL is disabled, the USB communication will cease to function.
```