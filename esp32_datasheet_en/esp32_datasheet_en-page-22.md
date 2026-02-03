**Title: Boot Configurations**

The chip allows for configuring the following boot parameters through strapping pins and eFuse bits at power-up or a hardware reset, without microcontroller interaction.

- **Chip boot mode**
  - Strapping pin: GPIO0 and GPIO2

- **Internal LDO (VDD_SDIO) Voltage**
  - Strapping pin: MTDI
  - eFuse bit: EFUSE_SDIO FORCE and EFUSE_SDIO TIEH

- **UOTXD printing**
  - Strapping pin: MTDO and GPIO5

- **Timing of SDIO Slave**
  - Strapping pin: MTDO and GPIO5

- **JTAG signal source**
  - eFuse bit: EFUSEDISABLE JTAG

The default values of all the above eFuse bits are 0, which means that they are not burnt. Given that eFuse is one-time programmable, once an eFuse bit is programmed to 1, it can never be reverted to 0. For how to program eFuse bits, please refer to ESP32 Technical Reference Manual > Chapter eFuse Controller.

The default values of the strapping pins, namely the logic levels, are determined by pins’ internal weak pull-up/pull-down resistors at reset if the pins are not connected to any circuit, or connected to an external high-impedance circuit.

**Table 3-1. Default Configuration of Strapping Pins**

| Strapping Pin | Default Configuration | Bit Value |
|---------------|------------------------|-----------|
| GPIO0         | Pull-up                | 1         |
| GPIO2         | Pull-down              | 0         |
| MTDI          | Pull-down              | 0         |
| MTDO          | Pull-up                | 1         |
| GPIO5         | Pull-up                | 1         |

To change the bit values, the strapping pins should be connected to external pull-down/pull-up resistances. If the ESP32 is used as a device by a host MCU, the strapping pin voltage levels can also be controlled by the host MCU.

All strapping pins have latches. At system reset, the latches sample the bit values of their respective strapping pins and store them until the chip is powered down or shut down. The states of latches cannot be changed in any other way. It makes the strapping pin values available during the entire chip operation, and the pins are freed up to be used as regular IO pins after reset.

The timing of signals connected to the strapping pins should adhere to the setup time and hold time specifications in Table 3-2 and Figure 3-1.

**Footer:**
Espressif Systems
ESP32 Series Datasheet v5.2

Submit Documentation Feedback