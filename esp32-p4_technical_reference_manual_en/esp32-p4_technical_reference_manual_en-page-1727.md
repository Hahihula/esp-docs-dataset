

```markdown
Chapter 36 Image Signal Processor (ISP)  

Register 36.119. ISP_AF_LUM_C_REG (0x0160)  

| 31 | 28 | 27 | ... | 0 |  
|----|----|----|-----|---|  
| O  | O  | O  |     | Reset |  

ISP_AF_LUMC Represents the luminance statistics from AF window C. (RO)  


Register 36.120. ISP_AWBO_WHITE_CNT_REG (0x017C)  

| 31 | ... | 24 | 23 | ... | 0 |  
|----|-----|----|----|-----|---|  
| O  | O   | O  | O  |     | Reset |  

ISP_AWBO_WHITE_CNT Represents the number of white patches within the AWB statistical window. (RO)  


Register 36.121. ISP_AWBO_ACC_R_REG (0x0180)  

| 31 | ... | 0 |  
|----|-----|---|  
|    |     | Reset |  

ISP_AWBO_ACC_R Represents the accumulated value of the R component for white patches within the AWB statistical window. (RO)  


Register 36.122. ISP_AWBO_ACC_G_REG (0x0184)  

| 31 | ... | 0 |  
|----|-----|---|  
|    |     | Reset |  

ISP_AWBO_ACC_G Represents the accumulated value of the G component for white patches within the AWB statistical window. (RO)  


Epressif Systems                          1727          ESP32-P4 TRM  
Submit Documentation Feedback             PRELIMINARY
```