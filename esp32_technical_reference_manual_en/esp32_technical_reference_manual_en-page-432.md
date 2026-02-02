**Title:**
Chapter 22 I2S Controller (I2S)

**Subtitle:**
22.8 Registers

**Body Text:**
The addresses in this section are relative to the I2S base address provided in Table 3.3-6 in Chapter 3 System and Memory. The absolute register addresses are listed in Section [22.7 Register Summary](#).

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

**Register Descriptions:**

1. **Register 22.1. I2S_FIFO_WR_REG (0x0000)**
   - Diagram:
     ```
     31    30    29    28    27    26    25    24    23    22    21    20    19    18    17    16    15    14    13    12    11    10    9     8     7     6     5     4     3     2     1     0
     0   | O   | O   | O   | O   | O   | O   | O   | O   | O   | O   | O   | O   | O   | O   | O   | O   | O   | O   | O   | O   | O   | O
     ```
   - Description: I2S_FIFO_WR_REG Writes the data sent by I2S into FIFO. (WO)

2. **Register 22.2. I2S_FIFO_RD_REG (0x0004)**
   - Diagram:
     ```
     31    30    29    28    27    26    25    24    23    22    21    20    19    18    17    16    15    14    13    12    11    10    9     8     7     6     5     4     3     2     1     0
     0   | O   | O   | O   | O   | O   | O   | O   | O   | O   | O   | O   | O   | O   | O   | O   | O   | O   | O   | O   | O   | O   | O
     ```
   - Description: I2S_FIFO_RD_REG Stores the data that I2S receives from FIFO. (RO)

**Footer:**
Espressif Systems  
432 ESP32 TRM (Version 5.6)  
Submit Documentation Feedback