**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Section Header:**
Register 30.3. SPI_USER_REG (0x0010)

**Continuation Note:**
Continued from the previous page...

**Subsection with Code and Description:**
- **SPI_USR_CONF_NXT (for SPI2 only)**
  - Enable the CONF state for the next transaction (segment) in a configurable segmented transfer. Can be configured in CONF state.
    - If this bit is set, it means this configurable segmented transfer will continue its next transaction (segment).
    - If this bit is cleared, it means this transfer will end after the current transaction (segment) is finished. Or this is not a configurable segmented transfer.

**Subsection with Code and Description:**
- **SPI_SIO**
  - Set the bit to enable 3-line half-duplex communication, where MOSI and MISO signals share the same pin.
    - 1: enable
    - 0: disable. Can be configured in CONF state (R/W)

**Subsection with Code and Description:**
- **SPI_USR_MISO_HIGHPART**
  - In read-data phase, only access to high-part of the buffers SPI_W8_REG ~ SPI_W15_REG.
    - 1: enable
    - 0: disable. Can be configured in CONF state (R/W)

**Subsection with Code and Description:**
- **SPI_USR_MOSI_HIGHPART**
  - In write-data phase, only access to high-part of the buffers SPI_W8_REG ~ SPI_W15_REG.
    - 1: enable
    - 0: disable. Can be configured in CONF state (R/W)

**Subsection with Code and Description:**
- **SPI_USR_DUMMY_IDLE**
  - If this bit is set, SPI clock is disabled in DUMMY state.
    - Can be configured in CONF state.

**Subsection with Code and Description:**
- **SPI_USR_MOSI**
  - Set this bit to enable the write-data (DOUT) state of an operation. 
    - Can be configured in CONF state

**Subsection with Code and Description:**
- **SPI_USR_MISO**
  - Set this bit to enable the read-data (DIN) state of an operation.
    - Can be configured in CONF state.

**Subsection with Code and Description:**
- **SPI_USR_DUMMY**
  - Set this bit to enable the DUMMY state of an operation. 
    - Can be configured in CONF state

**Subsection with Code and Description:**
- **SPI_USR_ADDR**
  - Set this bit to enable the address (ADDR) state of an operation.
    - Can be configured in CONF state.

**Subsection with Code and Description:**
- **SPI_USR_COMMAND**
  - Set this bit to enable the command (CMD) state of an operation. 
    - Can be configured in CONF state

**Footer Information:**
Espressif Systems
Page number: 1155
Document version: ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback