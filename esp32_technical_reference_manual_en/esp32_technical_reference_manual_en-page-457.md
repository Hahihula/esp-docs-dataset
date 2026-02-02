**Chapter Title:**
Chapter 23 Pulse Count Controller (PCNT)

**Section Titles and Content:**

1. **Register 23.1. PCNT_U[n]_CONFO_REG (n: 0-7) (0x0+0x0C*n)**
   - Continued from the previous page...
     - `PCNT_THRThRESO_ENUn`: This is the enable bit for unit n’s thres0 comparator. (R/W)
     - `PCNT_THRL_LIM_ENUn`: This is the enable bit for unit n’s thr_l_lim comparator. (R/W)
     - `PCNT_THRH_LIM_ENUn`: This is the enable bit for unit n’s thr_h_lim comparator. (R/W)
     - `PCNT_THRZERO_ENUn`: This is the enable bit for unit n’s zero comparator. (R/W)
     - `PCNT_FILTER_ENUn`: This is the enable bit for unit n’s input filter. (R/W)

2. **Register 23.2. PCNT_U[n]_CONF1_REG (n: 0-7) (0x4+0x0C*n)**
   - Diagram:
     ```
     +---------------------------+
     |                          |
     |                          |
     |                          |
     |                          |
     |                          |
     |                          |
     |                          |
     |                          |
     |                          |
     |                          |
     |                          |
     |                          |
     |                          |
     |                          |
     |                          |
     +---------------------------+
     ```
   - `PCNT_CNT_THRES1Un`: This register is used to configure the thresh1 value for unit n. (R/W)
   - `PCNT_CNTThRESOUn`: This register is used to configure the thres0 value for unit n. (R/W)

3. **Register 23.3. PCNT_U[n]_CONF2_REG (n: 0-7) (0x8+0x0C*n)**
   - Diagram:
     ```
     +---------------------------+
     |                          |
     |                          |
     |                          |
     |                          |
     |                          |
     |                          |
     |                          |
     |                          |
     |                          |
     |                          |
     |                          |
     |                          |
     |                          |
     |                          |
     |                          |
     +---------------------------+
     ```
   - `PCNT_CNT_L_LIM_Un`: This register is used to configure the thr_l_lim value for unit n. (R/W)
   - `PCNT_CNT_H_LIM_Un`: This register is used to configure the thr_h_lim value for unit n. (R/W)

**Footer:**
Espressif Systems
457 ESP32 TRM (Version 5.6)