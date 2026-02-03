**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Section Heading:**
Slave Segmented Transfer

**Subsection Titles and Content:**

1. **Full-duplex**
   - A data transfer controlled by DMA in SPI slave mode.
   - Such transfer consists of multiple transactions (segments).
   - The sending line and receiving line between the master and the slave are independent.

2. **Half-duplex**
   - Only one side, the master or the slave, sends data first,
   - And the other side receives data.
   - Sending data and receiving data cannot happen at the same time:
     - 4-line full-duplex: clock line (CS), CS line, two data lines. The four data lines can be used to send or receive data simultaneously.

3. **4-line half-duplex**
   - Clock line, CS line,
   - Two data lines.
   - Only one side of the communication is active at a time:
     - 3-line here means: clock line (CS), two data lines and no command signal; The three lines are used to transmit or receive.

4. **1-bit SPI**
   - In one clock cycle, bit can be transferred:

5. **(2-bit) Dual SPI**
   - A mode of dual SPI.
   - One in clock cycle,
   - Two bits (one from master and another slave).

6. **Dual Output Read**
   - Another data transfer method:
     - Command or two address bits.

7. **(4-bit) Quad SPI**
   - In one clock cycle, four bits can be transferred:

8. **Quad Output Read**
   - A mode of quad SPI.
   - One in clock cycle,
   - Four command (address).

9. **Quad I/O Read**
   - Another data transfer method:
     - Command or address.

10. **QPI** 
    - In one clock cycle, four bits can be transferred:

11. **(8-bit) Octal SPI**
    - A mode of octal SPI.
    - One in clock cycle,
    - Eight bits (address).

12. **Octal Output Read**
    - Another data transfer method:
     - Command or address.

13. **Octal I/O Read**
   - In one clock cycle, eight bits can be transferred:

14. **OPI** 
    - A mode of octal SPI.
    - One in clock cycle,
    - Eight bits (address).

15. **FSPI**

16. **SPI3**

**Footer:**
Espressif Systems
Page number 1107, Document version ESP32-S3 TRM (Version 1.7)