**Title:**
Chapter 38 Pulse Count Controller (PCNT)

**Header:**
Register 38.6, PCNT_U[7]_STATUS_REG (n: 0-3) (0x0050+0x4*n)

**Binary Representation Diagram:**
A binary representation of a register with bits labeled from n=0 to n=3.

**Body Text and Descriptions for Each Bit Field in the Register:**

1. **PCNT_CNT_THR_ZERO_MQDE_U[n]**
   - Description:
     The pulse counter status of PCNT_U[n] corresponding to 0.
   - Values (in decimal):
     0: pulse counter decreases from positive to O.
     1: pulse counter increases from negative to O.
     2: pulse counter is negative.
     3: pulse counter is positive. (RO)

2. **PCNT_CNT_THRThRES1_LAT_U[n]**
   - Description:
     The latched value of thres1 event of PCNT_U[n] when threshold event interrupt is valid.
   - Values (in decimal):
     0: the current pulse counter equals to thres1 and thres1 event is valid. 
     1: others
     RO

3. **PCNT_CNT_THRThRESO_LAT_U[n]**
   - Description:
     The latched value of thres0 event of PCNT_U[n] when threshold event interrupt is valid.
   - Values (in decimal):
     0: the current pulse counter equals to thres0 and thres0 event is valid. 
     1: others
     RO

4. **PCNT_CNT_THR_L_LIM_LAT_U[n]**
   - Description:
     The latched value of low limit event of PCNT_U[n] when threshold event interrupt is valid.
   - Values (in decimal):
     0: the current pulse counter equals to thr_lim and low limit event is valid. 
     1: others
     RO

5. **PCNT_CNT_THR_H_LIM_LAT_U[n]**
   - Description:
     The latched value of high limit event of PCNT_U[n] when threshold event interrupt is valid.
   - Values (in decimal):
     0: the current pulse counter equals to thr_h_lim and high limit event is valid. 
     1: others
     RO

6. **PCNT_CNT_THR_ZERO_LAT_U[n]**
   - Description:
     The latched value of zero threshold event of PCNT_U[n] when threshold event interrupt is valid.
   - Values (in decimal):
     0: the current pulse counter equals to O and zero thresh-old event is valid. 
     1: others
     RO

**Footer Information:**
Espressif Systems  
Page number: 1450  
Document version: ESP32-S3 TRM (Version 1.7)  
Link for submitting documentation feedback.

**Navigation Link:** GoBack