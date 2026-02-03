**Title:**
Table 30.5-8. Registers Used for State Control in 1/2/4/8-bit Modes

**Columns Headers:**

- **State:** 
  - Mode FSPI/SPI3 Bus (CMD, ADDR, DUMMY, DIN, DOUT)
  
- **Control Registers for 1-bit Mode FSPI/SPI3 Bus**
  
- **Control Registers for 2-bit Mode FSPI/SPI3 Bus**
  
- **Control Registers for 4-bit Mode FSPI/SPI3 Bus**
  
- **Control Registers for 8-bit Mode FSPI/SPI3 Bus**

**Rows:**

1. **CMD:** 
   - SPI_USR_COMMAND_VALUE
   - SPI_USR_COMMAND_BITLEN
   - SPI_FCMD_DUAL
   - SPI_USR_COMMAND
   - SPI_USR_COMMAND_VALUE
   - SPI_USR_COMMAND_BITLEN
   - SPI_FCMD_QUAD
   - SPI_FCMD_OCT

2. **ADDR:** 
   - SPI_USR_ADDR_VALUE
   - SPI_USR_ADDR_BITLEN
   - SPI_FADR_DUAL
   - SPI_USR_ADDR
   - SPI_USR_ADDR_VALUE
   - SPI_FADRBITEN
   - SPI_FADR_QUAD
   - SPI_FADR_OCT

3. **DUMMY:** 
   - SPI_USRDummy_CYCLELEN
   - SPI_USRDummy_CYCLELEN
   - SPI_USRDummy
   - SPI_USR_DUMMY
   - SPI_USRDummy_CYCLELEN
   - SPI_USRDUMMY
   - SPI_USRDummy
   - SPI_USRDUMMY

4. **DIN:** 
   - SPI_USRMISO
   - SPI_MS_DATA_BITLEN
   - SPI_FREAD_DUAL
   - SPI_USRMISO
   - SPI_MS_DATA_BITLEN
   - SPI_FREAD_QUAD
   - SPI_FREAD_OCT

5. **DOUT:** 
   - SPI_USRMOSI
   - SPI_MS_DATA_BITLEN
   - SPI_FWRITE_DUAL
   - SPI_USRMOSI
   - SPI_MS_DATA_BITLEN
   - SPI_FWRITE_QUAD
   - SPI_FWRITE_OCT

**Footer:**
ESP32-S3 TRM (Version 1.7)