**Title:**
3 Boot Configurations

**Body Text:**

The chip allows for configuring the following boot parameters through strapping pins and eFuse parameters at power-up or a hardware reset, without microcontroller interaction.

- **Chip boot mode**
  - Strapping pins: GPIO0 and GPIO46

- **VDD_SPI voltage**
  - Strapping pin: GPIO45
  - eFuse parameters: EFUSE_VDD_SPI FORCE and EFUSE_VDD_SPI_TIEH

- **ROM message printing**
  - Strapping pin: GPIO46
  - eFuse parameters: EFUSE_UART_PRINT_CONTROL and EFUSE_UART_PRINT_CHANNEL

The default values of all the above eFuse parameters are 0, which means that they are not burnt. Given that eFuse is one-time programmable, once programmed to 1, it can never be reverted to 0. For how to program eFuse parameters, please refer to ESP32-S2 Technical Reference Manual > Chapter eFuse Controller.

The default values of the strapping pins, namely the logic levels, are determined by pins’ internal weak pull-up/pull-down resistors at reset if the pins are not connected to any circuit, or connected to an external high-impedance circuit.

**Table:**
Title 3-1. Default Configuration of Strapping Pins

| Strapping Pin | Default Configuration    | Bit Value |
|---------------|---------------------------|----------|
| GPIO0         | Weak pull-up             | 1        |
| GPIO45        | Weak pull-down           | 0        |
| GPIO46        | Weak pull-down           | 0        |

To change the bit values, the strapping pins should be connected to external pull-down/pull-up resistances. If the ESP32-S2 is used as a device by a host MCU, the strapping pin voltage levels can also be controlled by the host MCU.

All strapping pins have latches. At system reset, the latches sample the bit values of their respective strapping pins and store them until the chip is powered down or shut down. The states of latches cannot be changed in any other way. It makes the strapping pin values available during the entire chip operation, and the pins are freed up to be used as regular IO pins after reset.

The timing of signals connected to the strapping pins should adhere to the setup time and hold time specifications in Table 3-2 and Figure 3-1.

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32-S2 Series Datasheet v1.8