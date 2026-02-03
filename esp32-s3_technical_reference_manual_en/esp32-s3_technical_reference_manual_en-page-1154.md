**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Register Information:**
- Register Name: SPI_USER_REG (0x0010)
- Diagram Description:
  - The diagram shows the bit layout of the SPI_USER_REG register with labels for each bit position from 32 to 0.
  - Bits are labeled as follows, starting at top and moving down left-to-right in groups:

    ```
    SPI_USER_COMMAND
    SPI_USER_ADDR
    SPI_USER_MISO
    (reserved)
    SPI_USER_MOSI
    SPI_USER_SCK
    SPI_USER_CS
    SPI_USER_DUMMY
    SPI_USER_IDLE_HIGHPART
    SPI_USER_IDLE_LOWPART
    SPI_USER_OPL
    SPI_USER_QPI
    SPI_USER_FIRMWARE
    SPI_USER_FIRMWARE_2
    (reserved)
    SPI_USER_FIRMWARE_3
    SPI_USER_FIRMWARE_4
    SPI_USER_FIRMWARE_5
    SPI_USER_FIRMWARE_6
    SPI_USER_FIRMWARE_7
    SPI_USER_FIRMWARE_8
    SPI_USER_FIRMWARE_9
    SPI_USER_FIRMWARE_10
    SPI_USER_FIRMWARE_11
    SPI_USER_FIRMWARE_12
    SPI_USER_FIRMWARE_13
    SPI_USER_FIRMWARE_14
    SPI_USER_FIRMWARE_15
    SPI_USER_FIRMWARE_16
    SPI_USER_FIRMWARE_17
    SPI_USER_FIRMWARE_18
    SPI_USER_FIRMWARE_19
    SPI_USER_FIRMWARE_20
    SPI_USER_FIRMWARE_21
    SPI_USER_FIRMWARE_22
    SPI_USER_FIRMWARE_23
    SPI_USER_FIRMWARE_24
    SPI_USER_FIRMWARE_25
    SPI_USER_FIRMWARE_26
    SPI_USER_FIRMWARE_27
    SPI_USER_FIRMWARE_28
    SPI_USER_FIRMWARE_29
    SPI_USER_FIRMWARE_30
    SPI_USER_FIRMWARE_31
    ```

**Bit Description:**
- `SPI_OUTDIN`: Set the bit to enable full-duplex communication. 1: enable, 0: disable.
- `SPI_QPI_MODE`: Enable QPI mode (1) or Disable it when using SPI controller as master or slave; can be configured in CONF state.

**Subsections and Descriptions of Each Bit:**
1. **SPI_OPI_MODE**: 
   - Description for SPI2 only, enables OPI mode.
   - Can configure the SPI controller to work with all 8-bit modes (R/W).

2. **SPI_TSCK_I_EDGE**: 
   - In slave mode; can support four different clocking methods described in Subsection 30.7.3.

3. **SPI_CS_HOLD**:
   - Keeps CS low when SPI is done.
   - Can be configured to hold the chip select line (R/W).

4. **SPI_CS_SETUP**: 
   - Enables or disables SPI CS during preparation state; can configure in CONF state for R/W operations.

5. **SPI_RSCK_I_EDGE**: 
   - In slave mode, supports four different clocking methods described in Subsection 30.7.3 (R/W).

6. **SPI_CK_OUT_EDGE**:
   - Used with SPI_MOSI_DELAY_MODE to set MOSI signal delay; can configure for R/W operations.

7. **SPI_FWRITE_DUAL**: 
   - In write and read data phases, operates in 2-bit mode.
   - Can be configured from CONF state (R/W).

8. **SPI_FWRITE_QUAD**:
   - In write operation with quad data transfer; can configure for R/W operations.

9. **SPI_FWRITE_OCT**: 
   - For SPI2 only: enables or disables read data phase in 8-bit mode.
   - Can be configured from CONF state (R/W).

**Footer Information:**
- "Continued on the next page..."
- Page number and document version information:
  - Espressif Systems
  - ESP32-S3 TRM (Version 1.7)
  - Submit Documentation Feedback

This detailed description captures all textual content from the image, including headings, descriptions of each bit in the register layout diagram, subsections for specific configurations or modes related to SPI operations within a microcontroller context provided by Espressif Systems' documentation on ESP32-S3 TRM.