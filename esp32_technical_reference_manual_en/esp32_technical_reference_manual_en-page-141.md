**Chapter Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**GoBack Link:** GoBack

---

**Register Section Header:**

- **Register Name**: Register 6.12. GPIO_ENABLE1_W1TC_REG (0x0034)
  - **Description**: 
    - `GPIO_ENABLE_DATA` GPIO32-39 output enable clear register.
    - For every bit that is 1 in the value written here, the corresponding bit in GPIO_ENABLE1 will be cleared. (WO)

- **Register Name**: Register 6.13. GPIO_STRAP_REG (0x0038)
  - **Description**:
    - `GPIO_STRAPPING` GPIO strapping results: Bit5-bit0 of boot_sel_chip[5:0] correspond to MTDI, GPI00, GPI02, GPI04, MTDO, GPI05, respectively.

- **Register Name**: Register 6.14. GPIO_IN_REG (0x003c)
  - **Description**:
    - `GPIO_IN` GPIO00-31 input value.
    - Each bit represents a pin input value; 1 for high level and 0 for low level. (RO)

- **Register Name**: Register 6.15. GPIO_IN_1_REG (0x0040)
  - **Description**:
    - `GPIO_IN_DATA` GPIO32-39 input value.
    - Each bit represents a pin input value; 1 for high level and 0 for low level.

---

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback

--- 

**Binary Representation of Registers in the Image:** 
- The image shows binary representations with some bits marked as `Reset` or unspecified, but these are not part of any specific register description and should be ignored for content extraction purposes.

---

**Note:**
The registers described here seem to relate specifically to GPIO (General Purpose Input/Output) configuration settings in the context of an ESP32 microcontroller. The binary representations shown might correspond to different states or configurations, but they are not detailed enough without additional documentation on their specific meanings within each register's scope.

--- 

**Markdown Format:**

```markdown
# Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

## GoBack

### Register Section:

- **Register Name**: Register 6.12. GPIO_ENABLE1_W1TC_REG (0x0034)
  - **Description**: 
    - `GPIO_ENABLE_DATA` GPIO32-39 output enable clear register.
    - For every bit that is 1 in the value written here, the corresponding bit in GPIO_ENABLE1 will be cleared. (WO)

- **Register Name**: Register 6.13. GPIO_STRAP_REG (0x0038)
  - **Description**:
    - `GPIO_STRAPPING` GPIO strapping results: Bit5-bit0 of boot_sel_chip[5:0] correspond to MTDI, GPI00, GPI02, GPI04, MTDO, GPI05, respectively.

- **Register Name**: Register 6.14. GPIO_IN_REG (0x003c)
  - **Description**:
    - `GPIO_IN` GPIO00-31 input value.
    - Each bit represents a pin input value; 1 for high level and 0 for low level. (RO)

- **Register Name**: Register 6.15. GPIO_IN_1_REG (0x0040)
  - **Description**:
    - `GPIO_IN_DATA` GPIO32-39 input value.
    - Each bit represents a pin input value; 1 for high level and 0 for low level.

---

Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback

```

--- 

**Binary Representation of Registers in the Image:**
- The image shows binary representations with some bits marked as `Reset` or unspecified, but these are not part of any specific register description and should be ignored for content extraction purposes.

---

**Note:** 
The registers described here seem to relate specifically to GPIO (General Purpose Input/Output) configuration settings in the context of an ESP32 microcontroller. The binary representations shown might correspond to different states or configurations, but they are not detailed enough without additional documentation on their specific meanings within each register's scope.

--- 

**Markdown Format:**

```markdown
# Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

## GoBack

### Register Section:

- **Register Name**: Register 6.12. GPIO_ENABLE1_W1TC_REG (0x0034)
  - **Description**: 
    - `GPIO_ENABLE_DATA` GPIO32-39 output enable clear register.
    - For every bit that is 1 in the value written here, the corresponding bit in GPIO_ENABLE1 will be cleared. (WO)

- **Register Name**: Register 6.13. GPIO_STRAP_REG (0x0038)
  - **Description**:
    - `GPIO_STRAPPING` GPIO strapping results: Bit5-bit0 of boot_sel_chip[5:0] correspond to MTDI, GPI00, GPI02, GPI04, MTDO, GPI05, respectively.

- **Register Name**: Register 6.14. GPIO_IN_REG (0x003c)
  - **Description**:
    - `GPIO_IN` GPIO00-31 input value.
    - Each bit represents a pin input value; 1 for high level and 0 for low level. (RO)

- **Register Name**: Register 6.15. GPIO_IN_1_REG (0x0040)
  - **Description**:
    - `GPIO_IN_DATA` GPIO32-39 input value.
    - Each bit represents a pin input value; 1 for high level and 0 for low level.

---

Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback

```