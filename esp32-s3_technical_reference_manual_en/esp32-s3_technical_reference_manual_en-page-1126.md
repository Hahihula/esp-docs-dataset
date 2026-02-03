**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**GoBack Link:** [GoBack](#)

**Body Text:**

As shown in Table **30.5-8**, the registers in each cell should be configured to set the FSPI/SPI3 bus to corresponding bit mode, i.e., the mode shown in the table header, at a specific state (corresponding to the first column).

**Configuration**

For instance, when GP-SPI reads data, and

- CMD is in 1-bit mode
- ADDR is in 2-bit mode
- DUMMY is 8 clock cycles
- DIN is in 4-bit mode

The register configuration can be as follows:

1. **Configure CMD state related registers:**
   - Configure the required command value in `SPI_USR_COMMAND_VALUE`.
   - Configure command bit length in `SPI_USR_COMMAND_BITLEN`. `SPI_USR_COMMAND_BITLEN` = expected bit length - 1.
   - Set `SPI_USR_COMMAND`.

2. **Configure ADDR state related registers:**
   - Configure the required address value in `SPI_USR_ADDR_VALUE`.
   - Configure address bit length in `SPI_USR_ADDR_BITLEN`. `SPI_USR_ADDR_BITLEN` = expected bit length - 1.
   - Set `SPI_USR_ADDR` and `SPI_FADDR_DUAL`.

3. **Configure DUMMY state related registers:**
   - Configure DUMMY cycles in `SPI_USRDummy_Cyclelen`. `SPI_USRDummy_Cyclelen` = expected clock cycles - 1.
   - Set `SPI_usr_DUMMY`.

4. **Configure DIN state related registers:**
   - Configure read data bit length in `SPI_MS_Data_BitLen`. `SPI_MS_Data_BitLen` = bit length expected - 1.
   - Set `SPI_FREAD_Quad` and `SPI_usr_MISO`.
   - Clear `SPI_FREAD_DUAL`.

5. **Configure GDMA in DMA-controlled mode:**
   - In CPU controlled mode, no action is needed.

6. **Clear registers:** 
   - Clear `SPI_USR_MOSI`.

7. **Set registers to start GP-SPI transfer:**
   - Set `SPI_usr` and other necessary registers (e.g., `SPI_DMA_AFIFO_RST`, `SPI_BUF_AFIFO_RST`, etc.) as needed.

**Footer Information:**

Espressif Systems  
Page Number: 1126  
Document Title: ESP32-S3 TRM (Version 1.7)  
Link to Submit Documentation Feedback