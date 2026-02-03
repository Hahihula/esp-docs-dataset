**Chapter Title:**
Chapter 16 World Controller (WCL)

**Section Titles and Descriptions with Registers Information:**

- **Register 16.10, WCL_CORE_0_World_UPDATE_REG (0x0148)**
  - Description:
    ```
    WCL_CORE_O_UPDATE
    Write any value to this field to indicate the completion of CPUO configuration for switching from Secure World to Non-Secure World.
    ```

- **Register 16.11, WCL_CORE_0_World_Cancel_REG (0x014C)**
  - Description:
    ```
    WCL_CORE_O_CANCEL
    Write any value to this filed to cancel the CPUO configuration for switching from Secure World to Non-Secure World.
    ```

- **Register 16.12, WCL_CORE_0_World_IRam0_REG (0x0150)**
  - Description:
    ```
    WCL CORE O WORLD IRAMO
    Stores the world info of CPUO’s instruction bus. This field is only used for debugging.
    ```

**Footer:**
- Page Number and Document Information:
  ```
  Espressif Systems
  Submit Documentation Feedback
  ESP32-S3 TRM (Version 1.7)
  ```