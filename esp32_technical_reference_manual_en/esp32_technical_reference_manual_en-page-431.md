**Chapter Title:**
Chapter 22 I2S Controller (I2S)

**Table of Registers and Descriptions**

1. **I2S_OUT_LINK_REG**
   - Description: DMA transmit linked list configuration and address.
   - Address: 0x3FF4F030
   - Access Mode: R/W

2. **I2S_IN_LINK_REG**
   - Description: DMA receive linked list configuration and address.
   - Address: 0x3FF4F034
   - Access Mode: R/W

3. **I2S_OUT_EOF_DESC_ADDR_REG**
   - Description: The address of transmit link descriptor producing EOF.
   - Address: 0x3FF4F038
   - Access Mode: RO

4. **I2S_IN_EOF_DESC_ADDR_REG**
   - Description: The address of receive link descriptor producing EOF.
   - Address: 0x3FF4F03C
   - Access Mode: RO

5. **I2S_OUT_EOF_BFR_DESC_ADDR_REG**
   - Description: The address of transmit buffer producing EOF.
   - Address: 0x3FF4F040
   - Access Mode: R/W

6. **I2S_INLINK_DSCR_REG**
   - Description: The address of current inlink descriptor.
   - Address: 0x3FF4F048
   - Access Mode: RO

7. **I2S_INLINK_DSCR_BFO_REG**
   - Description: The address of next inlink descriptor.
   - Address: 0x3FF4F04C
   - Access Mode: R/W

8. **I2S_INLINK_DSCR_BF1_REG**
   - Description: The address of next inlink data buffer.
   - Address: 0x3FF4F050
   - Access Mode: RO

9. **I2S_OUTLINK_DSCR_REG**
   - Description: The address of current outlink descriptor.
   - Address: 0x3FF4F054
   - Access Mode: R/W

10. **I2S_OUTLINK_DESCR_BFO_REG**
    - Description: The address of next outlink descriptor.
    - Address: 0x3FF4F058
    - Access Mode: RO

11. **I2S_OUTLINK_DESCR_BF1_REG**
    - Description: The address of next outlink data buffer.
    - Address: 0x3FF4F05C
    - Access Mode: R/W

12. **I2S_LC_STATEO_REG**
    - Description: DMA receive status.
    - Address: 0x3FF4F06C
    - Access Mode: RO

13. **I2S_LC_STATE1_REG**
    - Description: DMA transmit status.
    - Address: 0x3FF4F070
    - Access Mode: R/W

**Pulse density (DE) modulation registers**

- I2S_PDM_CONF_REG
  - Description: PDM configuration.
  - Address: 0x3FF4FOB4
  - Access Mode: R/W

- I2S_PDM_FREQ_CONF_REG
  - Description: PDM frequencies.
  - Address: 0x3FF4FOB8
  - Access Mode: RO

**Interrupt registers**

- I2S_INT_RAW_REG
  - Description: Raw interrupt status.
  - Address: 0x3FF4F00C
  - Access Mode: R/W

- I2S_INT_ST_REG
  - Description: Masked interrupt status.
  - Address: 0x3FF4FO10
  - Access Mode: RO

- I2S_INT_ENA_REG
  - Description: Interrupt enable bits.
  - Address: 0x3FF4FO14
  - Access Mode: R/W

- I2S_INT_CLR_REG
  - Description: Interrupt clear bits.
  - Address: 0x3FF4F018
  - Access Mode: WO

**Footer Information**
- Page Number: 431
- Document Version: ESP32 TRM (Version 5.6)
- Company Name: Espressif Systems
- Link Texts:
  - Submit Documentation Feedback