**Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**GoBack**

---

**Register 6.15. GPIO_STRAP_REG (0x0038)**

- **Description:** 
  - `GPIO_STRAPPING` GPIO strapping values:
    - bit5 ~ bit2 correspond to strapping pins GPIO3, GPIO45,
    - GPIOO, and GPIO46 respectively.
    - (RO)

**Binary Representation:**
```
0 0 0 0 0 0 0 0 0 0
```

---

**Register 6.16. GPIO_IN_REG (0x003C)**

- **Description:** 
  - `GPIO_IN_DATA_NEXT`:
    - GPIOO ~ 31 input value.
    - Each bit represents a pin input value, 1 for high level and 0 for low level.
    - (RO)

**Binary Representation:**
```
0
```

---

**Register 6.17. GPIO_IN1_REG (0x0040)**

- **Description:** 
  - `GPIO_IN_DATA1_NEXT`:
    - GPIO32 ~ 48 input value.
    - Each bit represents a pin input value.
    - (RO)

**Binary Representation:**
```
0
```

---

**Footer Information:**
Espressif Systems  
506 ESP32-S3 TRM (Version 1.7)  

Submit Documentation Feedback