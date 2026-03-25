

```markdown
## 10.2.1 Default Configuration

The default values of the strapping pins, namely the logic levels, are determined by pins’ internal weak pull-up/pull-down resistors at reset if the pins are not connected to any circuit, or connected to an external high-impedance circuit.

Table 10.2-1. Default Configuration of Strapping Pins

| Strapping Pin | Default Configuration | Bit Value |
|---------------|------------------------|---------|
| GPIO25        | Floating               | –       |
| GPIO26        | Floating               | –       |
| GPIO27        | Pull-up                | 1       |
| GPIO28        | Pull-up                | 1       |
| GPIO7         | Floating               | –       |
| MTMS          | Floating               | –       |
| MTDI          | Floating               | –       |

To change the strapping bit values, users can apply external pull-down/pull-up resistors, or use host MCU GPIOs to control the voltage level of these pins when powering up ESP32-C5. After the reset is released, the strapping pins work as normal-function pins.

## 10.2.2 Chip Boot Mode Control

GPIO26, GPIO27 and GPIO28 control the boot mode after the reset is released. See Table 10.2-2 Boot Mode Control.

Table 10.2-2. Boot Mode Control

| Boot Mode                  | GPIO26   | GPIO27 | GPIO28 |
|-----------------------------|----------|--------|--------|
| SPI Boot¹                   | Any value| Any value| 1¹     |
| Joint Download Boot 0²      | Any value| Any value| 1      |
| Joint Download Boot 1³      | 0        | 0      | 0      |

---

¹ Bold marks the default value and configuration.

² Joint Download Boot 0 mode supports the following download methods:
   - USB-Serial-JTAG Download Boot
   - UART Download Boot

³ Joint Download Boot 1 mode supports the following download methods:
   - UART Download Boot
   - SDIO Download Boot

In SPI Boot mode, the ROM bootloader loads and executes the program from SPI flash to boot the system.

In Joint Download Boot 0 mode, users can download binary files into flash using UART0, USB, or SPI Slave interfaces. It is also possible to download binary files into SRAM and execute it from SRAM.
```