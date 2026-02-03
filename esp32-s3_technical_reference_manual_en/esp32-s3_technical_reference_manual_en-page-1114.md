**Title:**
Table S0-5, Bit Order Control in GP-SPI Master and Slave Modes

**Columns Headers:**
1. **Bit Mode:** FSPI Bus Signal | SPI_RD/WR_BIT_ORDER = 0 (MSB) | SPI_RD/WR_BIT_ORDER = 2 (MSB) | SPI_RD/WR_BIT_ORDER = 1 (LSB) | SPI_RD/WR_BIT_ORDER = 3 (LSB)
2. **Sub-headers:**
   - 1-bit mode
     - FSPIQ or FSPIQ' B7→B6→B5→B4→B3→B2→B1→BO
     - ...
   - 2-bit mode
     - FSPID, etc.
     - BO→B0→B8→...
   - 4-bit mode
     - FSPIQ or FSPIQ' B7→B6→B5→B4→B3→B2→B1→BO
     - ...
   - 8-bit mode
     - FSPID, etc.
     - BO→B0→...

**Content:**
- **1-bit mode:** 
  - FSPIQ or FSPIQ' B7→B6→B5→B4→B3→B2→B1→BO | ... | ...
  
- **2-bit mode:** 
  - FSPID, etc. (B6→B4→B3→B2→B0) to BO→B0→...
  
- **4-bit mode:**
  - FSPIQ or FSPIQ' B7→B6→B5→B4→B3→B2→B1→BO | ... | ...
  
- **8-bit mode:** 
  - FSPID, etc. (B0→B0→) to BO→B0→...

**Footer:**
ESP32-S3 TRM (Version 1.7)

**Side Texts:**
- "Submit Documentation Feedback" on the left side.
- Page number and navigation options ("Go Back") at the bottom right corner.

(Note: The ellipses (...) indicate that there is more content in each column, but it has been omitted for brevity.)