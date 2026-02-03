**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
18.1 EE.FFT.CMUL.S16.LD.XP

**Subsection Titles and Content:**

- **Instruction Word:** 
  - Lists various registers such as sel[2:1], qu[0], qy[2:0], etc.

- **Assembler Syntax:**
  - Example syntax provided for the instruction `EE.FFT.CMUL.S16.LD.XP`.

- **Description:**
  - Explanation of how this instruction performs a signed complex multiplication, similar to EE.CMUL.S16 but with different register order and operations. It involves loading lower bits from memory into registers and incrementing values based on the value in another register.

- **Operation (Code Block):**
  ```assembly
  if sel8 == 0:
    qz[ 15: 0 ] = (qx[ 15: 0 ] * qy[ 15: 0 ] + qx[ 31: 16 ] : SAR[5:0]
    qz[ 31: 16 ] = (qx[ 31: 16 ] * qy[ 15: 0 ] - qx[ 15: 0 ] : SAR[5:0]

  if sel8 == 1:
    qz[ 15: 0 ] = (qx[ 15: 0 ] * qy[ 31: 16 ] : SAR[5:0]
    qz[ 31: 16 ] = (qx[ 31: 16 ] * qy[ 15: 0 ] + qx[ 15: 0 ] : SAR[5:0]

  if sel8 == 2:
    qz[ 47: 32 ] = (qx[ 47: 32 ] * qy[ 47: 32 ] + qx[ 63: 48 ] : SAR[5:0]
    qz[ 63: 48 ] = (qx[ 63: 48 ] * qy[ 47: 32 ] - qx[ 47: 32 ] : SAR[5:0]

  if sel8 == 3:
    qz[ 47: 32 ] = (qx[ 47: 32 ] * qy[ 47: 32 ] + qx[ 63: 48 ] : SAR[5:0]
    qz[ 63: 48 ] = (qx[ 63: 48 ] * qy[ 47: 32 ] - qx[ 47: 32 ] : SAR[5:0]

  if sel8 == 4:
    qz[ 79: 64 ] = (qx[ 79: 64 ] * qy[ 79: 64 ] + qx[ 95: 80 ] : SAR[5:0]
    qz[ 95: 80 ] = (qx[ 95: 80 ] * qy[ 79: 64 ] - qx[ 95: 80 ] : SAR[5:0]

  if sel8 == 5:
    qz[ 79: 64 ] = (qx[ 79: 64 ] * qy[ 79: 64 ] + qx[ 95: 80 ] : SAR[5:0]
    qz[ 95: 80 ] = (qx[ 95: 80 ] * qy[ 79: 64 ] - qx[ 95: 80 ] : SAR[5:0]

  qu[127:0] = load128({as31:4,4{0}})
  as[31:0] = as[31:0] + ad[31:0]
  ```

**Footer Information:** 
- Company Name: Espressif Systems
- Document Version and Type: ESP32-S3 TRM (Version 1.7)
- Navigation Links: Submit Documentation Feedback, GoBack