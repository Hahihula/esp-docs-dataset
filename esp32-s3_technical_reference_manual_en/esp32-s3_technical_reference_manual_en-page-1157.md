**Title: Chapter 30 SPI Controller (SPI)**

**Subtitle: Register 30.6. SPI_CTRL_REG (0x0008)**

**Table Description:**  
The table lists various registers related to the SPI controller, each with a specific bit order and function.

- **Columns**: 
  - Bit Order
  - Function
  
- **Rows**:
  - `SPL_WB_BIT_ORDER` through `SPL_DUMMY_OUT`: These are different bits in the register that control or indicate various functions related to the SPI operations.
  
**Text Content:**

1. **SPI_DUMMY_OUT**
   - Can be configured in CONF state (R/W)
     - For SPI2:
       - 0: In DUMMY state, the FSPI bus signals are not output
       - 1: In DUMMY state, the FSPI bus signals are output

2. **For SPI3**  
   - In DUMMY state, the signal level of SPI is output by the SPI controller.

3. **SPI_FADDR_DUAL**
   - Apply 2-bit mode during address (ADDR) state.
     - 1: enable
     - 0: disable
     - Can be configured in CONF state (R/W)

4. **SPI_FADDR_QUAD**
   - Apply 4-bit mode during address (ADDR) state:
     - 1: enable
     - 0: disable
     - Can be configured in CONF state (R/W)

5. **SPI_FADDR_OCT**  
   - For SPI2 only
   - Apply 8-bit mode during address (ADDR) state.
     - 1: enable
     - 0: disable
     - Can be configured in CONF state (R/W)

6. **SPI_FCMD_DUAL**
   - Apply 2-bit mode during command (CMD) state:
     - 1: enable
     - 0: disable
     - Can be configured in CONF state (R/W)

7. **SPI_FCMD_QUAD**
   - Apply 4-bit mode during command (CMD) state.
     - 1: enable
     - 0: disable
     - Can be configured in CONF state (R/W)

8. **SPI_FCMD_OCT**  
   - For SP2 only
   - Apply 8-bit mode during command (CMD) state:
     - 1: enable
     - 0: disable
     - Can be configured in CONF state (R/W)

9. **SPI_FREAD_DUAL**
   - In read operations, read-data (DIN) state is in 2-bit mode.
     - 1: enable
     - 0: disable
     - Can be configured in CONF state (R/W)

10. **SPI_FREAD_QUAD**
    - In read operations, read-data (DIN) state is in 4-bit mode:
      - 1: enable
      - 0: disable
      - Can be configured in CONF state (R/W)

11. **SPI_FREAD_OCT**  
    - For SP2 only
    - In read operations, read-data (DIN) state is in 8-bit mode.
      - 1: enable
      - 0: disable
      - Can be configured in CONF state (R/W)

12. **SPI_Q_POL**
    - The bit is used to set MISO line polarity:
      - 1: high
      - 0: low
      - Can be configured in CONF state (R/W)

13. **SPI_D_POL**
    - The bit is used to set MOSI line polarity:
      - 1: high
      - 0: low
      - Can be configured in CONF state (R/W)

**Footer:**  
Continued on the next page...

**Document Information:**  
Espressif Systems  
Page number: 1157  
Document version: ESP32-S3 TRM (Version 1.7)  
Link to Submit Documentation Feedback