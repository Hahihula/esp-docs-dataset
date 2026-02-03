**Chapter Title:**
Chapter 16 World Controller (WCL)

**GoBack Link:** GoBack

---

**Section Header: Register Information**

- **Register Name and Address:**
  - **Register 16.13, WCL_CORE_0_World_DRamO_PIF_REG (0x0154)**
    - Description:
      ```
      Stores the world info of CPUO's data bus and peripheral bus.
      This field is only used for debugging. (R/W)
      ```

- **Register Name and Address:**
  - **Register 16.14, WCL_CORE_0_World_Phase_REG (0x0158)**
    - Description:
      ```
      Indicates if the CPUO is ready to switch from Non-secure World to Secure World.
      1: ready; 2: not ready. (RO)
      ```

- **Register Name and Address:**
  - **Register 16.15, WCL_CORE_0_NMI_MASK_ENABLE_REG (0x0180)**
    - Description:
      ```
      Write any value to this field to start CPUO masking any NMI interrupt.
      (WO)
      ```

---

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)

--- 

**Note:** The image also contains a diagram with binary values and labels, but the specific details of this diagram are not described in text form as per your instructions to only describe diagrams if they appear block or flowcharts which I understand from context here is just an array-like structure without any clear indication it's meant for representation.