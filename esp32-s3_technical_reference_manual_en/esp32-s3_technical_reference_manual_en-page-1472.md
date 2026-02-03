**Title: Chapter 39 On-Chip Sensors and Analog Signal Processing**

---

### Figure Caption:
- **Figure 39.3-7:** APB_SARADC_SAR1_PATT_TAB4_REG and Pattern Table Entry 12 - Entry 15

---

#### Body Text:

Each register consists of four 6-bit pattern table entries. Each entry is composed of two fields that contain ADC channel and attenuation information, as shown in **Table 39.3-8**.

| ch_sel | atten |
|--------|-------|
| x      |       |
| 5      | 2     |
| 1      | 0     |

---

### Figure Caption:
- **Figure 39.3-8:** Pattern Table Entry

#### Body Text:

attenuation: O: 0 dB; 1: 2.5 dB; 2: 6 dB; 3: 12 dB.

ch_sel ADC channel, see Table 39.3-1.

---

### Subtitle:
**39.3.7.5 Configuration Example for Multi-Channel Scanning**

#### Body Text:

In this example, the following channels are selected for multi-channel scanning for SAR ADC1:

- Channel 2, with the attenuation of 12 dB. See Figure **39.3-9**.
- Channel O, with the attenuation of 2.5 dB. See Figure **39.3-10**.

The detailed configuration is as follows:

#### List:
- Configure SAR ADC1:
  - Configure the first pattern table entry (cmd0, APB_SARADC_SAR1_PATT_TAB1_REG[5:0]):
    | ch_sel | atten |
    |--------|-------|
    | x      |       |
    | 5      | 2     |
    | 1      | 3     |

- Configure the second pattern table entry (cmd1, APB_SARADC_SAR1_PATT_TAB1_REG[11:6]):
  - atten write the value of 3 to this field, to set the attenuation to 12 dB.
  - ch_sel write the value of 2 to this field, to select channel 2 (see Table **39.3-1**).

---

### Figure Caption:
- **Figure 39.3-9:** SAR ADC1 cmd0 Configuration

---

### Figure Caption:
- **Figure 39.3-10:** SAR ADC1 cmd1 Configuration

---

#### Footer:

Espressif Systems  
Page number: 1472  
Document version: ESP32-S3 TRM (Version 1.7)  

Submit Documentation Feedback