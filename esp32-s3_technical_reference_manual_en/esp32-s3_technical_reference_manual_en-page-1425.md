**Chapter 37: Remote Control Peripheral (RMT)**

---

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| RMT_CHOSTATUS_REG | Channel O status register | 0x0050 | RO |
| RMT_CH1STATUS_REG | Channel 1 status register | 0x0054 | RO |
| RMT_CH2STATUS_REG | Channel 2 status register | 0x0058 | RO |
| RMT_CH3STATUS_REG | Channel 3 status register | 0x005C | RO |
| RMT_CH4STATUS_REG | Channel 4 status register | 0x0060 | RO |
| RMT_CH5STATUS_REG | Channel 5 status register | 0x0064 | RO |
| RMT_CH6STATUS_REG | Channel 6 status register | 0x0068 | RO |
| RMT_CH7STATUS_REG | Channel 7 status register | 0x006C | RO |

---

**Interrupt Registers**

- **RMT_INT_RAW_REG**: Raw interrupt status register
  - Address: 0x0070
  - Access: R/W/T/C/SS

- **RMT_INT_ST_REG**: Masked interrupt status register
  - Address: 0x0074
  - Access: RO

- **RMT_INT_ENA_REG**: Interrupt enable register
  - Address: 0x0078
  - Access: R/W

- **RMT_INT_CLR_REG**: Interrupt clear register
  - Address: 0x007C
  - Access: WT

---

**Carrier Wave Duty Cycle Registers**

- **RMT_CHOCARRIER_DUTY_REG**: Duty duty configuration register for channel O
  - Address: 0x0080
  - Access: R/W

- **RMT_CH1CARRIER_DUTY_REG**: Duty duty configuration register for channel 1
  - Address: 0x0084
  - Access: R/W

- **RMT_CH2CARRIER_DUTY_REG**: Duty duty configuration register for channel 2
  - Address: 0x0088
  - Access: R/W

- **RMT_CH3CARRIER_DUTY_REG**: Duty duty configuration register for channel 3
  - Address: 0x008C
  - Access: R/W

---

**TX Event Configuration Registers**

- **RMT_CHO_TX_LIM_REG**: Configuration register for channel O TX event | 0x00A0 | varies |
- **RMT_CH1_TX_LIM_REG**: Configuration register for channel 1 TX event | 0x00A4 | varies |
- **RMT_CH2_TX_LIM_REG**: Configuration register for channel 2 TX event | 0x00A8 | varies |
- **RMT_CH3_TX_LIM_REG**: Configuration register for channel 3 TX event | 0x00AC | varies |

**RMT_TX_SIM_REG**: RMT simultaneous TX register
  - Address: 0x00C4
  - Access: R/W

---

**RX Event Configuration Registers**

- **RMT_CH4_RX_LIM_REG**: Configuration register for channel 4 RX event
  - Address: 0x00B0
  - Access: R/W

- **RMT_CH5_RX_LIM_REG**: Configuration register for channel 5 RX event | 0x00B4 | varies |
- **RMT_CH6_RX_LIM_REG**: Configuration register for channel 6 RX event | 0x00B8 | varies |
- **RMT_CH7_RX_LIM_REG**: Configuration register for channel 7 RX event | 0x00BC | R/W

---

**Version Register**

- **RMT_DATE_REG**: Version control register
  - Address: 0x00CC
  - Access: R/W

---

*Espressif Systems*

*ESP32-S3 TRM (Version 1.7)*