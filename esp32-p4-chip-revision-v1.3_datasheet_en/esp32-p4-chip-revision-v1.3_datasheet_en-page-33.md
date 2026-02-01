**Title:**
3 Boot Configurations

**Body Text:**

The chip allows for configuring the following boot parameters through strapping pins and eFuse bits at power-up or a hardware reset, without microcontroller interaction.

- **Chip boot mode**
  - Strapping pin: GPIO35, GPIO36, GPIO37 and GPIO38
- **VDDO_FLASH Voltage**
  - eFuse bit: EFUSE_OPXA_TIEH_SEL_0
- **ROM message printing**
  - Strapping pin: GPIO36
  - eFuse bit: EFUSE_UART_PRINT_CONTROL
- **JTAG signal source**
  - Strapping pin: GPIO34
  - eFuse bit: EFUSE_DIS_PAD_JTAG, EFUSE_DIS_USB_JTAG, and EFUSE_JTAG_SEL_ENABLE

The default values of all the above eFuse bits are 0, which means that they are not burnt. Given that eFuse is one-time programmable, once an eFuse bit is programmed to 1, it can never be reverted to 0.

The default values of the strapping pins, namely the logic levels, are determined by pins' internal weak pull-up/pull-down resistors at reset if the pins are not connected to any circuit, or connected to an external high-impedance circuit.

**Table:**
Table 3-1. Default Configuration of Strapping Pins

| Strapping Pin | Default Configuration | Bit Value |
|---------------|------------------------|-----------|
| GPIO34        | Floating               | -         |
| GPIO35        | Weak pull-up           | 1         |
| GPIO36        | Floating               | -         |
| GPIO37        | Floating               | -         |
| GPIO38        | Floating               | -         |

To change the bit values, the strapping pins should be connected to external pull-down/pull-up resistors. If the ESP32-P4 is used as a device by a host MCU, the strapping pin voltage levels can also be controlled by the host MCU.

All strapping pins have latches. At chip reset, the latches sample the bit values of their respective strapping pins and store them until the chip is powered down or shut down. The states of latches cannot be changed in any other way. It makes the strapping pin values available during the entire chip operation, and the pins are freed up to be used as regular IO pins after reset.

The timing of signals connected to the strapping pins should adhere to the setup time and hold time specifications in Table 3-2 and Figure 3-1.

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32-P4 Series Datasheet v0.6