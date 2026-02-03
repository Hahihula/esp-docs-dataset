**Title: Chapter 3 GDMA Controller (GDMA)**

**Subtitle: Register 3.15. GDMA_OUT_INT_RAW_CHn_REG**

**Body Text with Code and Descriptions:**
- **GDMA_OUT_DONE_CHn_INT_RAW**: The raw interrupt bit turns to high level when the last data pointed by one transmit descriptor has been transmitted to peripherals for TX channel O.
(R/WTC/SS)

- **GDMA_OUT_EOF_CHn_INT_RAW**: The raw interrupt bit turns to high level when the last data pointed by one transmit descriptor has been read from memory for TX channel O. (R/WTC/SS)

- **GDMA_OUT_DSCR_ERR_CHn_INT_RAW**: The raw interrupt bit turns to high level when detecting transmit descriptor error, including owner error, the second and third word error of transmit descriptor for TX channel 0. (R/WTC/SS)

- **GDMA_OUT_TOTAL_EOF_CHn_INT_RAW**: The raw interrupt bit turns to high level when data corresponding a outlink (includes one descriptor or few descriptors) is transmitted out for TX channel O. (R/WTC/SS)

**Footer:**
Espressif Systems
386 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback

**Diagram Description in the Image:** The image contains a bit map with labels indicating different interrupt bits and their corresponding functions, such as GDMA_OUT_DONE_CHn_INT_RAW, GDMA_OUT_EOF_CHn_INT_RAW, etc., along with some reserved positions marked by "(reserved)". Each label is associated with specific binary values.