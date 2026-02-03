**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Titles and Content:**

- **SAR**
  The Shift Amount Register (SAR) stores the shift value in bits. There are two types of instructions in ESP32-S3’s extended instruction set that use SAR:
  - One is a type of instructions to shift vector data, including EE.VSR.32 and EE.VSL.32.
    - The former uses the lower 5 bits of SAR as the right-shift value,
    - And the latter uses the lower 5 bits of SAR as the left-shift value.

- **SAR_BYTE**
  The SAR_BYTE stores the shift value in bytes, a special register designed to handle non-aligned 128-bit data (see Section 1.5.3).
  For vector arithmetic instructions,
  - Data read or stored by extended instructions are forced to be 16-byte aligned.
    - In practice there is no guarantee that the data addresses used are always 16-byte aligned.

- **EE.LD.128.USAR.IP and EE.LD.128.USAR.XP**
  Instructions write the lower 4-bit values of memory access register to represent non-aligned data in SAR_BYTE while reading from ESP32-S3’s extended instruction set that use SAR_BYTE.
  - One is dedicated for handling non-aligned data, including EE.SRCQ.* and EE.SRC.Q*.

- **ACCC**
  Multiplier-accumulator. Instructions such as EE.VMULAS.*, ACCX*, or EE.SRS.ACCX are used during operations to accumulate all vector multiplication results of two QR registers.
  - The latter right shifts the ACCX register by the byte size in SAR_BYTE for a non-aligned address.

- **QACC_H, QACC_L**
  Successive accumulators partitioned segments. Instructions such as EE.VMULAS.*, QACC*, and EE.SRCMB* use these types of registers during operations.
  - These are mainly used to accumulate vector multiplication results into the corresponding segment parts (QACC_H and QACC_L).
    - The 16-bit vector multiplications result in segments respectively, with a total accumulation length for each.

- **FFT_BIT_WIDTH**
  This special register is dedicated to EE.BITREV instruction.
  - Indicates operating mode of EE.BITREV. 
  - Range from ~0 to ~7 indicating different bit-operating modes (3-bit and up).

**Footer:**
Espressif Systems
47 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback