**Title:**
3 Boot Configurations

**Body Text:**

The chip allows for configuring the following boot parameters through strapping pins, eFuse bits, and registers at power-up or a hardware reset, without microcontroller interaction.

- **Chip boot mode**
  - Strapping pin: GPIO8 and GPIO9
- ROM message printing
  - Strapping pin: GPIO8
  - eFuse bits: EFUSE_UART_PRINT_CONTROL and EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT
  - Register: LP_AON STORE4_REG[0]
- JTAG signal source
  - Strapping pin: GPIO25
  - eFuse bits: EFUSE_DIS_PAD_JTAG, EFUSE_DIS_USB_JTAG, and EFUSE_JTAG_SEL_ENABLE

The default values of all the above eFuse bits are O, which means that they are not burnt. Given that eFuse is one-time programmable, once an eFuse bit is programmed to 1, it can never be reverted to 0. For how to program eFuse bits, please refer to ESP32-H2 Technical Reference Manual > Chapter eFuse Controller.

The default values of the strapping pins, namely the logic levels, are determined by pins' internal weak pull-up/pull-down resistors at reset if the pins are not connected to any circuit, or connected to an external high-impedance circuit.

**Table Title:**
Table 3-1. Default Configuration of Strapping Pins

| Strapping Pin | Default Configuration | Bit Value |
|---------------|------------------------|-----------|
| GPIO8         | Floating               | —        |
| GPIO9         | Weak pull-up           | 1        |
| GPIO25        | Floating               | —        |

To change the bit values, the strapping pins should be connected to external pull-down/pull-up resistances. If the ESP32-H2 is used as a device by a host MCU, the strapping pin voltage levels can also be controlled by the host MCU.

All strapping pins have latches. At system reset, the latches sample the bit values of their respective strapping pins and store them until the chip is powered down or shut down. The states of latches cannot be changed in any other way. It makes the strapping pin values available during the entire chip operation, and the pins are freed up to be used as regular IO pins after reset.

The timing of signals connected to the strapping pins should adhere to the setup time and hold time specifications in Table 3-2 and Figure 3-1.

**Footer:**
Espressif Systems
Page number: 22

Link:
Submit Documentation Feedback