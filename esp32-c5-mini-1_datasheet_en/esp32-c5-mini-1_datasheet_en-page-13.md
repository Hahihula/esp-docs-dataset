Title: Boot Configurations

Note:
- The note states that this section is excerpted from "ESP32-C5 Series Datasheet" and refers to Section Boot Configurations. It also mentions Chapter 8 Module Schematics for strapping pin mapping between the chip and modules.

Body Text:

The chip allows for configuring the following boot parameters through strapping pins and eFuse parameters at power-up or a hardware reset, without microcontroller interaction.
- Chip boot mode
  - Strapping pin: GPIO26, GPIO27, and GPIO28

- SDIO sampling and driving clock edge
  - Strapping pin: GPIO25 and MTDI

- ROM message printing
  - Strapping pin: GPIO27
  - eFuse parameter: EFUSE_UART_PRINT_CONTROL and EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT

- JTAG signal source
  - Strapping pin: GPIO7
  - eFuse parameter: EFUSE_DIS_PAD_JTAG, EFUSE_DIS_USB_JTAG, and EFUSE_JTAG_SEL_ENABLE

The default values of all the above eFuse parameters are O, which means that they are not burnt. Given that eFuse is one-time programmable, once programmed to 1, it can never be reverted to 0. For how to program eFuse parameters, please refer to "ESP32-C5 Technical Reference Manual" > Chapter eFuse Controller.

The default values of the strapping pins, namely the logic levels, are determined by pins' internal weak pull-up/pull-down resistors at reset if the pins are not connected to any circuit, or connected to an external high-impedance circuit.

Table:
Title: Table 4-1. Default Configuration of Strapping Pins

| Strapping Pin | Default Configuration | Bit Value |
|---------------|------------------------|----------|
| GPIO25        | Floating               | –        |
| GPIO26        | Floating               | –        |
| GPIO27        | Pull-up                | 1        |
| GPIO28        | Pull-up                | 1        |
| GPIO7         | Floating               | –        |
| MTDIS         | Floating               | –        |

To change the bit values, the strapping pins should be connected to external pull-down/pull-up resistances.

Footer:
- Page number: "13"
- Company name and document version information at bottom right corner.