**Title:**
4 Boot Configurations

**Note:**  
The content below is excerpted from ESP32-C61 Series Datasheet > Section Boot Configurations. For the strapping pin mapping between the chip and modules, please refer to Chapter 8 Module Schematics.

**Body Text:**

The chip allows for configuring the following boot parameters through strapping-pins and eFuse parameter at power-up or a hardware reset, without microcontroller interaction.
- **Chip boot mode**
  - Strapping pin: GPIO8 and GPIO9
- SDIO sampling and driving clock edge
  - Strapping pin: MTDI and MTMS
- ROM message printing
  - Strapping pin: GPIO8
  - eFuse parameter: EFUSE_UART_PRINT_CONTROL and EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT
- JTAG signal source
  - Strapping pin: GPIO7
  - eFuse parameter: EFUSE_DIS_PAD_JTAG, EFUSE_DIS_USB_JTAG, and EFUSE_JTAG_SEL_ENABLE

The default values of all the above eFuse parameters are O, which means that they are not burnt. Given that eFuse is one-time programmable, once programmed to 1, it can never be reverted to O.

The default values of the strapping pins, namely the logic levels, are determined by pins’ internal weak pull-up/pull-down resistors at reset if the pins are not connected to any circuit, or connected to an external high-impedance circuit.

**Table:**
Title 5: Default Configuration of Strapping Pins

| Strapping Pin | Default Configuration | Bit Value |
|---------------|------------------------|-----------|
| MTMS          | Floating               | –         |
| MTDI          | Floating               | –         |
| GPIO7         | Floating               | –         |
| GPIO8         | Floating               | –         |
| GPIO9         | Pull-up                | 1         |

To change the bit values, the strapping pins should be connected to external pull-down/pull-up resistances. If the ESP32-C61 is used as a device by a host MCU, the strapping pin voltage levels can also be controlled by the host MCU.

All strapping pins have latches. At system reset, the latches sample the bit values of their respective strapping pins and store them until the chip is powered down or shut down. The states of latches cannot be changed in

**Footer:**
Espressif Systems  
14  
Submit Documentation Feedback  
ESP32-C61-MINI-1 & MINI-1U Datasheet v0.6