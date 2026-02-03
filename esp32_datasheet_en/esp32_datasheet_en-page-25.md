**Title: Boot Configurations**

---

### Section Title

#### Subsection Heading (3.3)

**UOTXD Printing Control**
During booting, the strapping pin MTDO can be used to control the UOTXD Printing, as Table 3-4 shows.

| **Table 3-4. UOTXD Printing Control** |
|----------------------------------------|
| | MTDO |
| Enabled | 1 |
| Disabled | 0 |

*Note:* Bold marks the default value and configuration.

---

#### Subsection Heading (3.4)

**Timing Control of SDIO Slave**
The strapping pin MTDQ and GPIO5 can be used to control the timing of SDIO slave, see Table 3-5 Timing Control of SDIO Slave.

| **Table 3-5. Timing Control of SDIO Slave** |
|---------------------------------------------|
| | MTDO | GPI05 |
| Falling edge sampling, falling edge output | 0 | 0 |
| Falling edge sampling, rising edge output | 0 | 1 |
| Rising edge sampling, falling edge output | 1 | 0 |
| Rising edge sampling, rising edge output | 1 | 1 |

*Note:* Bold marks the default value and configuration.

---

#### Subsection Heading (3.5)

**JTAG Signal Source Control**
If EFUSE_DISABLE_JTAG is set to 1, the source of JTAG signals can be disabled.

--- 

**Footer:**

Espressif Systems  
ESP32 Series Datasheet v5.2

Submit Documentation Feedback