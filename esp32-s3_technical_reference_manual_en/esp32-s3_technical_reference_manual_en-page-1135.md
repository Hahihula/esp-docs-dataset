**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Section Header and Subsection with Content:**

- **Subsection:** GP-SPI Works as a Slave

  - **Content:**
    - "GP-SPI can be used as a slave to communicate with an SPI master. As a slave, GP-SPI supports 1-bit SPI, 2-bit dual SPI, 4-bit quad SPI, and QPI modes, with specific communication formats. To enable this mode, set SPI_SLAVE_MODE in register SPI_SLAKE_REG."
    - "The CS signal must be held low during the transmission, and its falling/rising edges indicate the start/end of a single or segmented transfer."

- **Note:**
  - The length of transferred data must be in unit of bytes; otherwise extra bits will be lost. These additional bits mean that if there are any remaining bits after dividing by 8 (the result is not an integer), they should also include them.

- **Subsection:** Communication Formats

  - **Content:**
    - "In GP-SPI slave mode, SPI full-duplex and half-duplex communications are available. To select from the two communications, configure SPI_DOUTDIN in register SPI_USER_REG."
    - "Full-duplex communication means that input data and output data are transmitted simultaneously throughout the entire transaction. All bits are treated as input or output data which means no command, address or dummy states is expected. The interrupt SPITransDoneInt is triggered once the transaction ends."

  - **Details of each state:**
    - CMD:
      - "Indicate the function of SPI slave;"
      - "One byte from master to slave;"
      - "Only values in Table 30.5-14 and Table 30.5-15 are valid;"
      - "Can be sent in 1-bit SPI mode or 4-bit QPI mode."
    - ADDR:
      - "The address for WrBUF and RdBUF commands in CPU-controlled transfer, or placeholder bits in other transfers and can be defined by application;"
      - "One byte from master to slave;"
      - "Can be sent in 1-bit, 2-bit or 4-bit modes (according to the command)."
    - DUMMY:
      - No specific details provided.

**Footer:**
- Expressif Systems
- ESP32-S3 TRM (Version 1.7)
- Submit Documentation Feedback

**Navigation Links and Additional Information:**
- GoBack button at top right corner.
- Page number "1135" is visible near the bottom center of the page.

(Note: The text provided includes all readable content from the image, but it does not include any diagrams or visual elements that are described in detail.)