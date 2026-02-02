**Chapter Title:**
Chapter 5 eFuse Controller (EFUSE)

**GoBack Link:** GoBack

---

### Register Section:

- **Register Name and Address:**
  - EFUSE_BLK0_WDATA1_REG (0x020)
  
  **Description of the register field:**
  - This field programs the value of lower 32 bits of WIFI_MAC_Address.
  - **Field Description:** 
    ```
    0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
    ```

- **Register Name and Address:**
  - EFUSE_BLK0_WDATA2_REG (0x024)
  
  **Description of the register field:** 
  - This is reserved.
  - **Field Description:** 
    ```
    0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
    ```

- **Register Name and Address:**
  - EFUSE_WIFI_MAC_CRC_HIGH
  
  **Description of the register field:** 
  - This field programs the value of higher 24 bits of WIFI_MAC_Address.
  - **Field Description:** 
    ```
    0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
    ```

- **Register Name and Address:**
  - EFUSE_BLK0_WDATA3_REG (0x028)
  
  **Description of the register field:** 
  - These are the first three bits among the four bits to program chip packaging version.
  - **Field Description:** 
    ```
    12 11 9 8 6 4 3 2 1 0
    ```

- **Register Name and Address:**
  - EFUSE_CHIP_VER_PKG
  
  **Description of the register field:** 
  - This is reserved.
  - **Field Description:** 
    ```
    0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
    ```

- **Register Name and Address:**
  - EFUSE_SPI_PAD_CONFIG_HD
  
  **Description of the register field:** 
  - This field programs the value of SPI_pad_config_hd.
  - **Field Description:** 
    ```
    0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
    ```

- **Register Name and Address:**
  - EFUSE_CHIP_VER_DIS_CACHE
  
  **Description of the register field:** 
  - This field is programmed to disable cache.
  - **Field Description:** 
    ```
    0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
    ```

- **Register Name and Address:**
  - EFUSE_CHIP_VER_PKG
  
  **Description of the register field:** 
  - This is the fourth bit among the four bits to program chip packaging version.
  - **Field Description:** 
    ```
    0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
    ```

- **Register Name and Address:**
  - EFUSE_CHIP_VER_DIS_BT
  
  **Description of the register field:** 
  - This field is programmed to disable Bluetooth.
  - **Field Description:** 
    ```
    0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
    ```

- **Register Name and Address:**
  - EFUSE_CHIP_VER_DIS_APP_CPU
  
  **Description of the register field:** 
  - This field is programmed to disable APP CPU.
  - **Field Description:** 
    ```
    0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
    ```

---

**Footer:**
Espressif Systems  
107  
ESP32 TRM (Version 5.6)  

Submit Documentation Feedback