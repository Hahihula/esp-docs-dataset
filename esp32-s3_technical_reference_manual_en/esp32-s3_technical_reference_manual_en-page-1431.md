**Chapter Title:**
Chapter 37 Remote Control Peripheral (RMT)

**GoBack Link:** GoBack

---

**Register Information and Descriptions**

- **Register Name**: RMT_CHm_RXCARRIER_RM_REG  
  - **Address Range**: m = 4, 5, 6, 7; Address: Ox0090, Ox0094, Ox0098, Ox009C
  - **Field Description**:
    - `RMT_CARRIER_HIGH_THRES_CHm`: The high level period in a carrier modulation mode is (RMT_CARRIER_HIGHThRES_CHm + 1) for channel m. (R/W)
    - `RMT_CARRIER_LOW_THRES_CHm`: The low level period in a carrier modulation mode is (RMT_CARRIER_LOWThRES_CHm + 1) for channel m.

- **Register Name**: RMT_SYS_CONF_REG  
  - **Address Range**: Ox00C0
  - **Field Description**:
    - `RMT_CLK_EN`: 
      - `1'h1`: Access memory directly (NONFIFO mode).
      - `1'h0`: Access memory by FIFO (FIFO mode). (R/W)
    - `RMT_MEM_CLK FORCE_ON`: Set this bit to enable the clock for RMT memory. (R/W)
    - `RMT_MEM_FORCE_PD`: Set this bit to power down RMT memory. (R/W)
    - `RMT_MEM_FORCE PU`: Disable the power-down function of RMT memory in Light-sleep mode.
      - `0`: Power down RMT memory when RMT is in Light-sleep mode.

- **Additional Fields**:
  - `RMT_SCLK_DIV_NUM`: The integral part of the fractional divider. (R/W)
  - `RMT_SCLK_DIV_A`: The numerator of the fractional part of the fractional divider.
  - `RMT_SCLK_DIV_B`: The denominator of the fractional part of the fractional divider.

- **Clock Source Selection**:
  - `RMT_SCLK_SEL`:
    - Choose the clock source of rmt_sclk. 
      - `1`: APB_CLK
      - `2`: RC_FAST_CLK
      - `3`: XTAL_CLK

- **Fractional Clock Enable**:
  - `RMT_SCLK_ACTIVE`: rmt_sclk switch.
  - `RMT_CLK_EN`:
    - `0`: Power down the drive clock of registers. (R/W)

---

**Footer Information:**
Espressif Systems  
Page Number: 1431  
Document Title: ESP32-S3 TRM (Version 1.7)  
Link to Submit Documentation Feedback