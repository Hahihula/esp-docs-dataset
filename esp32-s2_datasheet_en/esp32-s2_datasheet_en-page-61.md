**Title: Glossary**

- **module**
  - A self-contained unit integrated within the chip to extend its capabilities, such as cryptographic modules.
  - RF modules [2]

- **peripheral**
  - A hardware component or subsystem within the chip to interface with the outside world.

- **in-package flash**
  - Flash integrated directly into the chip’s package, and external to the chip die. 

- **off-package flash**
  - Flash external to the chip's package [16]

- **strapping pin**
  - A type of GPIO pin used to configure certain operational settings during the chip’s power-up, and can be reconfigured as normal GPIO after the chip’s reset.

- **eFuse parameter**
  - A parameter stored in an electrically programmable fuse (eFuse) memory within a chip. The parameter can be set by programming EFUSE_PGM_DATA_n_REG registers, and read by reading a register field named after the parameter [29]

- **SPI boot mode**
  - A boot mode in which users load and execute the existing code from SPI flash.

- **joint download boot mode**
  - A boot mode in which users can download code into flash via the UART or other interfaces (see Table Chip Boot Mode Control >Note), and load and execute the downloaded code from the flash or SRAM [30]

**Footer:**
Espressif Systems
ESP32-S2 Series Datasheet v1.8

[Submit Documentation Feedback]