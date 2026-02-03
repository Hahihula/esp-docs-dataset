**Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**GoBack**

**Section Title:** Register 39.34, SENS_SAR_TOUCHThres13_reg (0x0094)

- **Field Description**: 
  - **Register Name**: SENS TOUCH OUT THRES13
  - **Description**: Finger threshold for touch pin 13.
  - **Access Mode**: Read/Write

**Binary Representation:**
```
0 0 0 0 0 0 D   0x0000    Reset
```

**Section Title:** Register 39.35, SENS_SAR_TOUCHThres14_reg (0x0098)

- **Field Description**: 
  - **Register Name**: SENS TOUCH OUT THRES14
  - **Description**: Finger threshold for touch pin 14.
  - **Access Mode**: Read/Write

**Binary Representation:**
```
0 0 0 0 0 0 D   0x0000    Reset
```

**Section Title:** Register 39.36, SENS_SAR_TOUCH_CHN_ST_REG (0x009C)

- **Field Description**: 
  - **Register Name**: SENS TOUCH MEAS DONE
  - **Description**: Touch measurement done.
  - **Access Mode**: Read Only

**Binary Representation:**
```
31 30 29   15 14    0     Reset
```

- **Fields within the register include:**
  - SENS TOUCH CHANNEL CLR (Clear touch channel. Write Only)
  - SENS TOUCH PAD ACTIVE (Touch active status. Read Only)

**Footer Information:** 
Espressif Systems  
ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback