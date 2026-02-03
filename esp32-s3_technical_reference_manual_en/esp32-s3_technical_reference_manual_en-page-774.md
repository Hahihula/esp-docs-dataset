**Title: Chapter 15 Permission Control (PMS)**

---

### Register Information:

- **Register 15.64**: PMS_CORE_0_VECBASE OVERRIDE_LOCK_REG (0x01B8)
  - Description:
    ```
    PMS_CORE_0_VECBASE OVERRIDE_LOCK
    ```
  - Bit description: 
    ```
    Set this bit to lock CPUO VECBASE configuration register.
    (R/W)
    ```

- **Register 15.65**: PMS_CORE_0_VECBASE OVERRIDE_0_REG (0x01BC)
  - Description:
    ```
    PMS CORE O_VECBASE OVERRIDE O REG
    ```
  - Bit description: 
    ```
    Set this bit so CPU uses WORLD0_VALUE in Secure World and Non-secure World. Clear this bit so CPU uses WORLD0_VALUE in Secure World and WORLD1_VALUE in Non-secure World.
    (R/W)
    ```

---

**Footer Information:**  
ESP32-S3 TRM | Version 1.7

**Navigation Links:**
- Submit Documentation Feedback
- GoBack