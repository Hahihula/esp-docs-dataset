**Title:**
3 Boot Configurations

**Body Text:**

The chip allows for configuring the following boot parameters through strapping pins and eFuse parameters at power-up or a hardware reset, without microcontroller interaction.

- **Chip boot mode**
  - Strapping pin: GPIO26, GPIO27, and GPIO28
- SDIO sampling and driving clock edge
  - Strapping pin: GPIO25 and MTDI
- ROM message printing
  - Strapping pin: GPIO27
  - eFuse parameter: EFUSE_UART_PRINT_CONTROL and EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT
- JTAG signal source
  - Strapping pin: GPIO7
  - eFuse parameter: EFUSE_DIS_PAD_JTAG, EFUSE_DIS_USB_JTAG, and EFUSE_JTAG_SEL_ENABLE

The default values of all the above eFuse parameters are 0, which means that they are not burnt. Given that eFuse is one-time programmable, once programmed to 1, it can never be reverted to O. For how to program eFuse parameters, please refer to ESP32-C5 Technical Reference Manual > Chapter eFuse Controller.

The default values of the strapping pins, namely the logic levels, are determined by pins’ internal weak pull-up/pull-down resistors at reset if the pins are not connected to any circuit, or connected to an external high-impedance circuit.

**Table Title:**
Table 3-1. Default Configuration of Strapping Pins

| Strapping Pin | Default Configuration | Bit Value |
|---------------|------------------------|-----------|
| GPIO25        | Floating               | –         |
| GPIO26        | Floating               | –         |
| GPIO27        | Pull-up                | 1         |
| GPIO28        | Pull-up                | 1         |
| GPIO7         | Floating               | –         |
| MTMS          | Floating               | –         |
| MTDI          | Floating               | –         |

To change the bit values, the strapping pins should be connected to external pull-down/pull-up resistances.

All strapping pins have latches. At Chip Reset, the latches sample the bit values of their respective strapping pins and store them until the chip is powered down or shut down. The states of latches cannot be changed in any other way. It makes the strapping pin values available during the entire chip operation, and the pins are freed up to be used as regular I/O pins after reset. For details on Chip Reset, see ESP32-C5 Technical Reference Manual > Chapter Reset and Clock.

**Footer:**
Espressif Systems
Page 29 of ESP32-C5 Series Datasheet v1.0

Submit Documentation Feedback