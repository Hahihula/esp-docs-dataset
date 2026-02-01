**Title: Boot Configurations**

The chip allows for configuring the following boot parameters through strapping pins and eFuse parameters at power-up or a hardware reset, without microcontroller interaction.

- **Chip boot mode**
  - Strapping pins: GPIO2, GPIO8, and GPIO9

- **ROM message printing**
  - Strapping pin: GPIO8
  - eFuse parameters: EFUSE_UART_PRINT_CONTROL and EFUSE_USB_PRINT_CHANNEL

The default values of all the above eFuse parameters are 0, which means that they are not burnt. Given that eFuse is one-time programmable, once programmed to 1, it can never be reverted to 0. For how to program eFuse parameters, please refer to ESP32-C3 Technical Reference Manual > Chapter eFuse Controller.

The default values of the strapping pins, namely the logic levels, are determined by pins' internal weak pull-up/pull-down resistors at reset if the pins are not connected to any circuit, or connected to an external high-impedance circuit.

**Table 3-1. Default Configuration of Strapping Pins**

| Strapping Pin | Default Configuration | Bit Value |
|---------------|------------------------|-----------|
| GPIO2         | Floating               | –         |
| GPIO8         | Floating               | –         |
| GPIO9         | Weak pull-up           | 1         |

To change the bit values, the strapping pins should be connected to external pull-down/pull-up resistances. If the ESP32-C3 is used as a device by a host MCU, the strapping pin voltage levels can also be controlled by the host MCU.

All strapping pins have latches. At Chip Reset, the latches sample the bit values of their respective strapping pins and store them until the chip is powered down or shut down. The states of latches cannot be changed in any other way. It makes the strapping pin value available during the entire chip operation, and the pins are freed up to be used as regular IO pins after reset. For details on Chip Reset, see ESP32-C3 Technical Reference Manual > Chapter Reset and Clock.

The timing of signals connected to the strapping pins should adhere to the setup time and hold time specifications in Table 3-2 and Figure 3-1.

**Table 3-2. Description of Timing Parameters for the Strapping Pins**

| Parameter | Description                                    | Min (ms) |
|-----------|------------------------------------------------|----------|
| tSU       | Setup time is the time reserved for the power rails to stabilize before the CHIP_EN pin is pulled high to activate the chip. | 0        |
| thH       | Hold time is the time reserved for the chip to read the strapping pin values after CHIP_EN is already high and before these pins start operating as regular IO pins. | 3        |

Espressif Systems  
ESP32-C3 Series Datasheet v2.2

**Submit Documentation Feedback**

Page number: **30**