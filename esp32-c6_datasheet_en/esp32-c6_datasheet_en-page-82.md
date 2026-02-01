**Title: Glossary**

- **module**
  - A self-contained unit integrated within the chip to extend its capabilities, such as cryptographic modules.
  - RF modules [2](#)

- **peripheral**
  - A hardware component or subsystem within the chip to interface with the outside world.

- **off-package flash**
  - Flash external to the chip's package. References: "4", "32", "40"

- **in-package flash**
  - Flash integrated directly into the chip’s package, and external to the chip die.
  - Reference: [32](#)

- **strapping pin**
  - A type of GPIO pin used to configure certain operational settings during the chip's power-up. Can be reconfigured as normal GPIO after the chip's reset.

- **eFuse parameter**
  - A parameter stored in an electrically programmable fuse (eFuse) memory within a chip.
  - The parameter can be set by programming EFUSE_PGM_DATA[ ]_REG registers, and read by reading a register field named after the parameter. Reference: [33](#)

- **SPI boot mode**
  - A boot mode in which users load and execute the existing code from SPI flash.

- **joint download boot mode**
  - A boot mode where you can download code into flash via the UART or other interfaces.
  - References:
    - "Chip Boot Mode Control" > Note
    - [34](#)

- **eFuse**
  - An onetime programmable (OTP) memory which stores system and user parameters, such as MAC address, chip revision number, flash encryption key etc. Value indicates the default state.
  - References:
    - "0": Indicates that eFuse has been programmed [40](#)

**Footer:**
- Espressif Systems
- Submit Documentation Feedback

**Page Number:** 
82 ESP32-C6 Series Datasheet v1.4