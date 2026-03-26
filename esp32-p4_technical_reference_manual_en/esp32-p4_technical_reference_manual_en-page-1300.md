

```markdown
Register 20.68. HP_SYSTEM_HP_CORE_DMACTIVE_LPCORE_REG (0x01A0)

HP_SYSTEM_CORE_DMACTIVE_LPCORE Represents the dmactive value of LP CPU's debug module.
O: Indicates that the LP CPU is not connected to the JTAG interface, or is not in debug mode.
1: Indicates that the LP CPU is connected to the JTAG interface and is in debug mode.
(RO)

Register 20.69. HP_SYSTEM_HP_CORE_ERR_RESP_DIS_REG (0x01A4)

HP_SYSTEM_CORE_ERR_RESP_DIS Configures whether or not to disable the error response on different buses.
Bit 0: IBUS
Bit 1: DBUS
Bit 2: AHB bus
(R/W)
```