**Title: Chapter 22 Digital Signature (DS)**

---

### Register 22.4. DS_SET_FINISH_REG (0x0E08)

- **Description:** Write 1 to this register to end DS operation.
- **Bit Pattern Diagram**: 
  - Reset state is shown with all bits set to '0'.
  - Set state shows the bit at position `31` as '1'.

---

### Register 22.5. DS_QUERY BUSY_REG (0x0E0C)

- **Description:** The DS peripheral status.
- **Bit Pattern Diagram**: 
  - Reset state is shown with all bits set to '0'.
  - Set state shows the bit at position `31` as '1'.

#### Details:
- **DS_QUERY BUSY_1:** Indicates if the DS peripheral is busy (1) or idle (0).

---

### Register 22.6. DS QUERY KEY WRONG REG (0x0E10)

- **Description:** Status of HMAC activation and recognition.
- **Bit Pattern Diagram**: 
  - Reset state shows all bits set to '0'.
  - Set states show the bit at positions `3`, `4`, or `5` as '1'.

#### Details:
- **DS_QUERY KEY WRONG_15:** Indicates if HMAC was activated but DS peripheral did not successfully receive the DS_KEY from the HMAC peripheral (value of 15).
- **DS_QUERY KEY WRONG_0:** Indicates if HMAC is not activated.

---

**Footer:**
- Espressif Systems
- Page number: 906
- Document version: ESP32-S3 TRM (Version 1.7)
- Link to submit documentation feedback