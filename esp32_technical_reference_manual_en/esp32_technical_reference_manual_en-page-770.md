**Title: Programming Reserved Register Field**

**GoBack**

---

### Introduction

A field in a register is reserved if the field is not open to users, or produces unpredictable results if configured to values other than defaults.

---

### Programming Reserved Register Field

The reserved fields should not be modified. It is not possible to write only part of a register since registers must always be written as a whole. As a result, to write an entire register that contains reserved fields, you can choose one of the following two options:

1. Read the value of the register, modify only the fields you want to configure and then write back the value so that reserved fields are untouched.

OR

2. Modify only the fields you want to configure and write back the default value of the reserved fields. The default value of a field is provided in the "Reset" line of a register diagram. For example, the default value of Field_A in `Register X` is 1:

   ```
   Register 31.35. Register X (Address)
   
   [Field C]    [Field B]    [Field A]
   31          20         19        16       15
   ```

   Suppose you want to set `Field_A`, `Field_B`, and `Field_C` of `Register X` to `0x0, 0x1,` and `0x2`, respectively:

   ```
   [Field A]    [Field B]    [Field C]
   31          20         19        16       15
   ```

   - Use option 1 and fill in the reserved fields with the value you have just read. Suppose the register reads as `0x0000_0003`. Then, you can modify the fields you want to configure, thus writing `0x0002_0002` to the register.

   - Use option 2 and fill in the reserved fields with their defaults. Thus, writing `0x0002_0002` to the register:

     ```
     [Field A]    [Field B]    [Field C]
     31          20         19        16       15
     ```

---

**Footer:**
Espressif Systems  
770 ESP32 TRM (Version 5.6)  

Submit Documentation Feedback