**Chapter Title:**
Chapter 12 DPort Registers

**GoBack Link:** GoBack

---

**Register Information and Descriptions:**

- **Register Name**: Register 12.22, DPORTE WIFI RST EN REG (0x0D0)
  - **Description**: 
    - `DPORTEMAC_RST`: Set the bit to reset Ethernet MAC module.
    - Clear the bit to release Ethernet MAC module.

- **Register Name**: DPORT_SDIO_HOST_RST
  - **Description**:
    - Set the bit to reset SD/MMC module.
    - Clear the bit to release SD/MMC module. (R/W)

- **Register Name**: DPORTE_SDIO_RST
  - **Description**:
    - Set the bit to reset SDIO module.
    - Clear the bit to release SDIO module.

---

**Register Information and Descriptions:**

- **Register Name**: Register 12.23, DPORT_CPU_INTR_FROM_CPU_n REG (n:0-3) (0xDC+4*n)
  - **Description**:
    - `DPORTECPUINTRFROMCUPART`: Interrupt in both CPUs.

---

**Register Information and Descriptions:**

- **Register Name**: Register 12.24, DPORT_PRO_INTR_STATUS_REG_n REG (n:0-2) (0xEC+4*n)
  - **Description**:
    - `DPORTEPROINTRSTATUSREG`: PRO_CPU interrupt status.

---

**Register Information and Descriptions:**

- **Register Name**: Register 12.25, DPORT_APP_INTR_STATUS_REG_n REG (n:0-2) (0xF8+4*n)
  - **Description**:
    - `DPORTEAPPINTRSTATUSREG`: APP_CPU interrupt status.

---

**Footer Information:**
Espressif Systems
Submit Documentation Feedback

ESP32 TRM (Version 5.6)

Page Number: 257