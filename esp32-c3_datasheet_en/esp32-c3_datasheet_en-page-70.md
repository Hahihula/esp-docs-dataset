**Title: Glossary**

- **chip series**
  - A subset of chips within a chip series group with similar core features and specifications (page references: 2, 68)

- **chip series group**
  - A broad group of related chip products that use the same die. For example, ESP32-C3 chip series group consists of ESP32-C3 chip series and ESP865 chip series (page reference: 2), with additional references to page numbers.

- **in-package flash**
  - Flash integrated directly into the chip's package, and external to the chip die (page number).

- **off-package flash**
  - Flash external to the chip’s package (page reference: 4)

- **peripheral**
  - A hardware component or subsystem within the chip to interface with the outside world (page references: 16, 19)

- **strapping pin**
  - A type of GPIO pin used to configure certain operational settings during the chip's power-up, and can be reconfigured as normal GPIO after the chip’s reset (page reference).

- **eFuse parameter**
  - A parameter stored in an electrically programmable fuse (eFuse) memory within a chip. The parameter can be set by programming EFUSE_PGM_DATA_n_REG registers, and read by reading a register field named after the parameter.

- **SPI boot mode**
  - A boot mode in which users load and execute the existing code from SPI flash (page reference).

- **joint download boot mode**
  - A boot mode in which users can download code into flash via the UART or other interfaces (see Table Chip Boot Mode Control > Note), and load and execute the downloaded code from the flash or SRAM.

- **eFuse**
  - A one-time programmable (OTP) memory which stores system and user parameters, such as MAC address, chip revision number, flash encryption key, etc. Value O indicates the default state, and value 1 indicates the eFuse has been programmed

**Footer:**
Espressif Systems
ESP32-C3 Series Datasheet v2.2