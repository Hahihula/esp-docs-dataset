**Title: Chapter 30 SPI Controller (SPI)**

---

### Section Title:
#### **30.5.7.2 Data Flow Control in Master Mode**

**Figure Caption:**  
*Figure 30.5-3. Data Flow Control in GP-SPI Master Mode*

**Body Text and Diagram Description for Figure:**
The diagram shows the data flow of GP-SPI in master mode, with control logic details:
- RX data (SPI rx\_afifo) is buffered by spi\_rx\_din\_ctrl.
- TX data from corresponding addresses according to transfer modes.

**Control Logic Details:**  
- CPU-controlled transfer for RX: stored at registers SPI\_WO\_REG ~ SPI\_W15\_REG
- DMA-controlled transfer for RX: stored in GDMA RX buffer

**TX Data Handling:**  
- CPU-controlled transfer for TX data from registers SPI\_WO\_REG ~ SPI\_W15\_REG.
- DMA-controlled transfer for TX data sent to GDMA TX buffer.

The timing module can be used with 1/2/4/8-bit modes, controlled by GP-SPI state machine. More information is available in Section 30.8.

---

### Section Title:
#### **30.5.7.3 Data Flow Control in Slave Mode**

**Figure Caption:**  
*Figure 30.5-4. Data Flow Control in GP-SPI Slave Mode*

**Body Text and Diagram Description for Figure:**
The diagram shows the data flow of GP-SPI in slave mode, with control logic details:
- RX data (SPI rx\_afifo) is buffered by spi\_slv\_din\_ctrl.
- TX data from corresponding addresses according to transfer modes.

**Control Logic Details:**  
- CPU-controlled transfer for RX: stored at registers SPI\_WO\_REG ~ SPI\_W15\_REG
- DMA-controlled transfer for RX: stored in GDMA RX buffer

**TX Data Handling:**  
- CPU-controlled transfer for TX data from registers SPI\_WO\_REG ~ SPI\_W15\_REG.
- DMA-controlled transfer for TX data sent to GDMA TX buffer.

The timing module can be used with 1/2/4/8-bit modes, controlled by GP-SPI state machine. More information is available in Section 30.8

---

**Footer:**
Espressif Systems  
Page number and document version note:
"1120 ESP32-S3 TRM (Version 1.7)"

**Action Link:** 
*Submit Documentation Feedback*

--- 

(Note: The text has been transcribed as accurately from the image, maintaining structure where possible.)