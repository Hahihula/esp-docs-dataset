**Chapter Title:**
Chapter 27 I2C Controller (I2C)

**GoBack Link:** GoBack

---

### Register Section:

- **Register Name and Address:**
  - `I2C COMMAND1 REG (0x005C)`

#### Description:
- **Field Name:**
  - `I2C_COMMAND1 DONE`
  
#### Details:
- This is the content of command register 1. It is the same as that of I2C_COMMAND.
- When command 1 has been executed in master mode, this bit changes to high level (R/W/SS).

---

### Register Section:

- **Register Name and Address:**
  - `I2C COMMAND2 REG (0x0060)`

#### Description:
- **Field Name:**
  - `I2C_COMMAND2 DONE`
  
#### Details:
- This is the content of command register 2. It is the same as that of I2C_COMMAND.
- When command 2 has been executed in master mode, this bit changes to high level (R/W/SS).

---

### Register Section:

- **Register Name and Address:**
  - `I2C COMMAND3 REG (0x0064)`

#### Description:
- **Field Name:**
  - `I2C_COMMAND3 DONE`
  
#### Details:
- This is the content of command register 3. It is the same as that of I2C_COMMAND.
- When command 3 has been executed in master mode, this bit changes to high level (R/W/SS).

---

**Footer:**
Espressif Systems
1035 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback