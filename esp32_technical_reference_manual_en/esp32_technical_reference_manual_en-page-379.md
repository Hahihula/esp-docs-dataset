**Title:**
Chapter 20 SPI Controller (SPI)

**Menu:**
GoBack

**Section Title and Description:**

- **Register 20.23. SPI_TX_CRC_REG (0xC0)**
  - Binary representation of the register is shown with all bits set to '0'.
  
- **SPI_TX_CRC_REG Reserved.**

- **Register 20.24. SPI_EXT2_REG (0xF8)**
  - Binary representation of the register, showing specific bit positions labeled as follows:
    - `3`
    - `2`
    - `1` with label "Reset"
  
**Subsection Title and Description:**

- **SPI_ST The current state of the SPI state machine: (RO)**

  | Bit Position | State |
  |--------------|-------|
  | 0           | idle state |
  | 1           | preparation state |
  | 2           | send command state |
  | 3           | send data state |
  | 4           | read data state |
  | 5           | write data state |
  | 6           | wait state |
  | 7           | done state |

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback