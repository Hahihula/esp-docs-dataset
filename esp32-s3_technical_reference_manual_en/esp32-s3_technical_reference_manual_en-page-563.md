**Chapter Title:**
Chapter 9 Interrupt Matrix (INTERRUPT)

**GoBack Link:** GoBack

**Register Information and Descriptions:**

1. **Interrupt Core1 Interrupt Status Register 2 (0x0994) - Register 9.177.**
   - **Name:** INTERRUPT_CORE1_INTR_STATUS_2
   - **Address:** 0x0994
   - **Description:** This register stores the status of the third 32 interrupt sources.
   - **Access Mode:** (RO)
   - **Reset Value:** 0

2. **Interrupt Core1 Interrupt Status Register 3 (0x0998) - Register 9.178.**
   - **Name:** INTERRUPT_CORE1_INTR_STATUS_3
   - **Address:** 0x0998
   - **Description:** This register stores the status of the last 3 interrupt sources.
   - **Access Mode:** (RO)
   - **Reset Value:** 0

3. **Interrupt Core1 Clock Gate Register (0x099C) - Register 9.179.**
   - **Name:** INTERRUPT_CORE1_CLOCK_GATE_REG
   - **Address:** 0x099C
   - **Description:** This register is used to control clock-gating of interrupt matrix.
   - **Access Mode:** (R/W)
   - **Reset Value:** Binary representation shown as "0 0 0 0 0 0 0 0" with a reset value indicated by the binary pattern.

**Footer:**
- Page Number: 563
- Document Title: ESP32-S3 TRM (Version 1.7)
- Company Name: Espressif Systems
- Link Texts:
   - Submit Documentation Feedback

(Note: The image contains a diagram at the bottom, but it is not described in detail as per your instructions.)