**Title:**
Table 30.5-3. FSPI bus Signals Used in Various SPI Modes

**Columns and Rows Description (from left to right, top to bottom):**

1. **FSPI Signal**: 
   - FD^1
   - FSPICLK
   - FSPICS0
   - FSPICS1
   - FSPICS2
   - FSPICS3
   - FSPICS4
   - FSPICS5
   - FSPID
   - FSPIQ
   - FSPIWP
   - FSPIHD
   - FSPIO4 ~ 7
   - FSPIDQS

2. **1-bit SPI**:
   - FD^2 (3-line HD)
     - Y, Y, Y, Y, Y, Y, Y, Y, Y, Y, Y, Y, Y, Y
  
3. **Dual SPI**:
   - 4-line HD
     - Y, Y, Y, Y, Y, Y, Y, Y, (Y)^3, (Y)^4, (Y)^5, (Y)^6

4. **Quad SPI**
   - QPI
     - V^7, V^8, V^9
  
5. **Octal SPI**:
   - OPI
     - Y, Y, Y, Y, Y, Y, Y, Y, Y, Y, Y, Y, Y

6. **1-bit SPI**
   - FD (3-line HD)
     - Y, Y, Y, Y, Y, Y, Y, Y, V^7, V^8, V^9
  
7. **Dual SPI**:
   - 4-line HD
     - Y, Y, Y, Y, Y, Y, Y, (Y)^6

8. **Quad SPI**
   - QPI
     - Y, Y, Y, Y, Y, Y, Y, V^10
  
9. **Slave Mode**:
   - FD (3-line HD)
     - Y, Y, Y, Y, Y, Y, Y, Y, Y, Y, Y, Y, Y

10. **Dual SPI**
    - 4-line HD
      - Y, Y, Y, Y, Y, Y, V^7
  
11. **Quad SPI**
    - QPI
      - (Y)^6, (Y)^8, (Y)^9
  
**Footnotes:**

- ^1 FD: full-duplex
- ^2 HD: half-duplex
- ^3 Only one of the two signals is used at a time.
- ^4 The two signals are used in parallel.
- ^5 The four signals are used in parallel.

**Additional Notes (below table):**
- 7. Only one of the two signals is used at a time.
- 8. The four signals are used in parallel

**Document Footer:**
ESP32-S3 TRM (Version 1.0)