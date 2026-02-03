**Chapter Title:**
Chapter 31 Two-wire Automotive Interface (TWAI®)

**GoBack Link:** GoBack

---

**Section Header - Register Address and Name:**
- **Register**: TWAI_ARB_LOST_CAP_REG (0x002C)
- **Description**: This register contains information about the bit position of lost arbitration.

**Binary Representation Diagram for TWAI_ARB_LOST_CAP:**
```
31  | 5 |
----|---|
0   | 4 |
----|---|
0   | 0 |
----|---|
0   | 0 |
----|---|
0   | 0 |
----|---|
0   | 0 |
```

**Section Header - Register Address and Name:**
- **Register**: TWAI_ERR_CODE_CAP_REG (0x030)
- **Description**: This register contains information about the location of errors, see Table 31.5 for details.

**Binary Representation Diagrams with Labels:**
- `TWAI_ERR_CODE_TYPE`
- `TWAI_ERR_CODE_DIRECTION`
- `TWAI_ERR_CODE_SEGMENT`

**Section Header - Register Address and Name:**
- **Register**: TWAI_ECC_SEGMENT
- **Description**: This register contains information about the location of errors, see Table 31.5 for details.

**Binary Representation Diagram with Labels:**
```
31  | 8 |
----|---|
0   | 7 |
----|---|
6   | 6 |
----|---|
5   | 4 |
----|---|
0   | 0 |
```

**Section Header - Register Address and Name:**
- **Register**: TWAI_ECC_DIRECTION
- **Description**: This register contains information about transmission direction of the node when error occurs. 
1: Error occurs when receiving a message; O: Error occurs when transmitting a message.

**Binary Representation Diagram with Labels:**
```
31  | 8 |
----|---|
0   | 7 |
----|---|
6   | 4 |
----|---|
5   | 0 |
```

**Section Header - Register Address and Name:**
- **Register**: TWAI_ECC_TYPE
- **Description**: This register contains information about error types:
00: bit error; O1: form error;
10: stuff error; 11: other type of error

**Binary Representation Diagram with Labels:**
```
31  | 8 |
----|---|
0   | 7 |
----|---|
6   | 4 |
----|---|
5   | 2 |
----|---|
0   | 0 |
```

**Section Header - Register Address and Name:**
- **Register**: TWAI_RX_ERR_CNT_REG (0x038)
- **Description**: The RX error counter register, reflects value changes in reception status.

**Binary Representation Diagram with Labels:**
```
31  | 8 |
----|---|
0   | 7 |
----|---|
6   | 4 |
----|---|
5   | 2 |
----|---|
0   | 0 |
```

**Section Header - Register Address and Name:**
- **Register**: TWAI_RX_ERR_CNT
- **Description**: The RX error counter register, reflects value changes in reception status.

**Binary Representation Diagram with Labels:**
```
31  | 8 |
----|---|
0   | 7 |
----|---|
6   | 4 |
----|---|
5   | 2 |
----|---|
0   | 0 |
```

**Footer Information:** 
- **Company**: Espressif Systems
- **Document Version**: ESP32-S3 TRM (Version 1.7)
- **Page Number**: 1223

**Action Links:**
- Submit Documentation Feedback