**Chapter 3: System and Memory**

---

### GoBack

0x4007_0000 ~ 0x4007_FFFF of the instruction bus. The remaining 128 KB can always be read and written by either CPU at addresses 0x4008_0000 ~ 0x4009_FFFF of instruction bus.

---

#### **3.3.2.4 Internal SRAM 1**

The capacity of Internal SRAM is 128 KB. Either CPU can read and write this memory at addresses
0x3FFE_0000 ~ 0x3FFF_FFFF of the data bus, and also at addresses 0x400A_0000 ~ 0x400B_FFFF of the instruction bus.

The address range accessed via the instruction bus is in reverse order (word-wise) compared to access via
the data bus. That is to say, address

- 0x3FFE_0000 and 0x400B_FFEC access the same word
- 0x3FEF_0004 and 0x400B_FF8 access the same word
- 0x3FFE_0008 ~ 0x400B_FF4 access the same word

...

- 0x3FFF_FFFC and 0x400A_0008 access the same word.

The data bus and instruction bus of the CPU are still both little-endian, so the byte order of individual words is not reversed between address spaces. For example,

- Address
  - 0x3FFE_0000 accesses the least significant byte in the word accessed by 0x400B_FFEC.
  - 0x3FEF_0001 accesses the second least significant byte in the word accessed by 0x400B_FFFC.
  - 0x3FEF_0002 accesses the second most significant byte in the word accessed by 0x400B_FFEC.
  - 0x3FEF_0003 accesses the most significant byte in the word accessed by 0x400B_FFFC.

...

- Address
  - 0x3FFE_FFFA accesses the second least significant byte in the word accessed by 0x400A_0004.
  - 0x3FFF_FFFB accesses the most significant byte in the word accessed by 0x400A_0004.

Part of this memory can be remapped onto the ROM O address space. See [Internal Rom](#) for more information.

---

#### **3.3.2.5 Internal SRAM 2**

The capacity of Internal SRAM is 200 KB. It can be read and written by either CPU at addresses
0x3FFA_E000 ~ 0x3FFD_FFFF on the data bus.
  
---

**Espressif Systems**
**69 ESP32 TRM (Version 5.6)**

[Submit Documentation Feedback](#)