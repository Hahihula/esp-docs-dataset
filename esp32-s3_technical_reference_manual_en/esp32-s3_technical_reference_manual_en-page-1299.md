**Chapter Title:**
Chapter 34 SD/MMC Host Controller (SDHOST)

**GoBack Link:** GoBack

**Register Information and Descriptions:**

- **Register Name:** Register 34.24. SDHOST_DEBNCE_REG (0x0064)
  - **Description:** 
    ```
    SDHOST_DEBOUNCE_COUNT
    Number of host clocks (clk) used by debounce filter logic.
    The typical debounce time is 5 ~ 25 ms to prevent the card instability when the card is inserted or removed. (R/W)
    ```

- **Register Name:** Register 34.25. SDHOST_USRID_REG (0x0068)
  - **Description:**
    ```
    SDHOST_USRID
    User identification register, value set by user.
    Can also be used as a scratch-pad register by user. (R/W)
    ```

- **Register Name:** Register 34.26. SDHOST_VERID_REG (0x006C)
  - **Description:**
    ```
    SDHOST_VERSIONID
    Hardware version register.
    Can also be read by fireware. (RO)
    ```

**Footer Information:**

- Company Logo and Name:
  - Espressif Systems

- Document Versioning Info:
  - ESP32-S3 TRM (Version 1.7)

- Page Number:
  - 1299

- Link for Submitting Documentation Feedback:
  - Submit Documentation Feedback