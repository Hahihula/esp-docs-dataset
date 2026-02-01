**Title: Boot Configurations**

The chip allows for configuring the following boot parameters through strapping pins and eFuse parameters at power-up or a hardware reset, without microcontroller interaction.

- **Chip boot mode**
  - Strapping pin: GPIO0 and GPIO46

- **VDD_SPI voltage**
  - Strapping pin: GPIO45
  - eFuse parameter: EFUSE_VDD_SPI FORCE and EFUSE_VDD_SPI_TIEH

- **ROM message printing**
  - Strapping pin: GPIO46
  - eFuse parameter: EFUSE_UART_PRINT_CONTROL and EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT

- **JTAG signal source**
  - Strapping pin: GPIO3
  - eFuse parameter: EFUSE_DIS_PAD_JTAG, EFUSE_DIS_USB_JTAG, and EFUSE_STRAP_JTAG_SEL

The default values of all the above eFuse parameters are O, which means that they are not burnt. Given that eFuse is one-time programmable; once programmed to I, it can never be reverted back.

**Table 3-1: Default Configuration of Strapping Pins**

| Strapping Pin | Default Configuration       | Bit Value |
|---------------|-------------------------------|-----------|
| GPIO0         | Weak pull-up                  | 1         |
| GPIO3         | Floating                      | –         |
| GPIO45        | Weak pull-down                | O         |
| GPIO46        | Weak pull-down                | O         |

To change the bit values, the strapping pins should be connected to external pull-down/pull-up resistances. If the ESP32-S3 is used as a device by a host MCU; the strapping pin voltage levels can also be controlled by the host MCU.

All strapping pins have latches. At Chip Reset, the latches sample the bit values of their respective strapping pins and store them until the chip is powered down or shut down. The states of latches cannot be changed in any other way; it makes the strap pin values available during the entire chip operation.
  
ESP32-S3 Technical Reference Manual > Chapter Reset and Clock.

**Footer:**
- Espresso Systems
- Page 32
- Submit Documentation Feedback

**Document Title:** ESP32-S3 Series Datasheet v2.1