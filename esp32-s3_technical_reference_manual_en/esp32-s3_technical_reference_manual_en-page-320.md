**Title: Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)**

---

### Section Header:
- **Operand Description - see Figure 2.5-17**

#### Body Text:
- **Rdst**: Destination Register R[0-3], results will be stored in this register.
- **Wait_Delay**: Number of cycles used to perform the measurement.

**Description:**
Increasing the measurement cycles Wait_Delay helps improve the accuracy and optimize the result. The instruction performs measurement via temperature sensor and stores the result into a general purpose register.

---

### Subtitle:
2.5.2.11 ADC – Take Measurement with ADC

---

#### Figure Caption (Figure 2.5-18):
**Instruction Type - ADC**

#### Table Title: 
Table 2.5-6. Input Signals Measured Using the ADC Instruction
| Pad/Signal/GPIO | Sar_Mux | ADC Selection (Sel) |
|------------------|---------|--------------------|
| GPIO1            | 1       |                    |
| GPIO2            | 2       |                    |
| GPIO3            | 3       |                    |
| GPIO4            | 4       |                    |
| GPIO5            | 5       | Sel = 0, select SAR ADC1 |
| GPIO6            | 6       |                    |
| GPIO7            | 7       |                    |
| GPIO8            | 8       |                    |
| GPIO9            | 9       |                    |
| GPIO10           | 10      | Sel = 1, select SAR ADC2 |
| GPIO11           | 1       |                    |
| GPIO12           | 2       |                    |
| GPIO13           | 3       |                    |
| GPIO14           | 4       |                    |
| XTAL_32k_P       | 5       | Sel = 1, select SAR ADC2 |
| XTAL_32k_N       | 6       |                    |
| GPIO17           | 7       |                    |
| GPIO18           | 8       |                    |
| GPIO19           | 9       |                    |
| GPIO20           | 10      | Sel = 1, select SAR ADC2 |

---

**Footer:**
Espressif Systems  
320 ESP32-S3 TRM (Version 1.7)  

Submit Documentation Feedback

--- 

*Note: The figure and table are described in detail as per the image content.*